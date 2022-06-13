// Called when the pipeline starts
// to verify the word is not an empty string
def verify_word(check_word) {
    def empty_word = (check_word =~ /^( )+$/) || ((params.word).length() == 0)

    if (empty_word) {
        error('Provided word is not valid')
    } else {
        echo('Checking word: ' + check_word)
    }
}

// Calls python inside the slave containers
// to check the meaning of the word
def get_word(check_word) {
    def word_output = sh(
        returnStdout: true,
        script: "echo $check_word | python3 ./Scripts/P06_GetMeaning.py"
    )
    
    return word_output
}

// Verifies the word has a short meaning
// and fails the stage "Search word" stage if meaning
// is not found
def show_word(word_output) {
    def meaning = (word_output =~ /((SHORT MEANING:( )+)(.*))/)

    if (!meaning) {
        error('No such word: ' + params.word)
    } else {
        echo meaning[0][4]
        currentBuild.warning = meaning[0][4]
    }
}

pipeline {
    agent none
    parameters {
        string(
            name: 'word',
            defaultValue: 'coffee',
            description: 'Enter a word to check in the dictionary'
        )
    }
    stages {
        stage('Verify param') {
            agent any
            steps {
                verify_word(params.word)
            }
        }
        stage('Pull script') {
            agent any
            steps {
                git 'https://github.com/OmkarPathak/Python-Programs.git'
                stash includes: 'Scripts/P06_GetMeaning.py', name: 'dict_script'
            }
        }
        stage('Search word') {
            parallel {
                stage('First container') {
                    agent { label 'dockerized_slave01' }
                    steps {
                        sh 'echo "Checking word in $(hostname)"'
                        unstash 'dict_script'
                        catchError(
                            buildResult: 'SUCCESS',
                            stageResult: 'FAILURE'
                        ) {
                            show_word(get_word(word))
                        }
                    }
                }
                stage('Second container') {
                    agent { label 'dockerized_slave02' }
                    steps {
                        sh 'echo "Checking word in $(hostname)"'
                        unstash 'dict_script'
                        catchError(
                            buildResult: 'SUCCESS',
                            stageResult: 'FAILURE'
                        ) {
                            show_word(get_word(word))
                        }
                    }
                }
                stage('Third container') {
                    agent { label 'dockerized_slave03' }
                    steps {
                        sh 'echo "Checking word in $(hostname)"'
                        unstash 'dict_script'
                        catchError(
                            buildResult: 'SUCCESS',
                            stageResult: 'FAILURE'
                        ) {
                            show_word(get_word(word))
                        }
                    }
                }
            }
        }
        
        // Continues to this "blank" stage
        // even if the "Search word" stage has failed
        stage ('Explanation') {
            agent any
            steps {
                echo 'View your word output in the previous stage'
            }
        }
    }
}
