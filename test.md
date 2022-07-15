<b>Installation params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--from-s3` | <p>Use S3 as a download source for AtScale images</p> | <p>-</p> | <p>-</p> | <p></p>
`--offline` | <p>Use the local configured repository as a download source for AtScale images</p> | <p>-</p> | <p>-</p> | <p></p>
`--os` | <p>Choose OS type for the AtScale containers</p> | <p>string</p> | <p>centos</p><p>centos8</p><p>ubuntu</p> | <p></p>
`--ip-address` | <p>Choose a custom subnet mask for the AtScale container group</p> | <p>string -> CIDR notation syntax</p> | <p>-</p> | <p></p>
`--no-network` | <p>Disables networking</p><p>This parameter has precedence over --with-network and --network-mode</p> | <p>-</p> | <p>-</p> | <p></p>
`--with-network` | <p>Expose containers network on the local machine</p> | <p>-</p> | <p>-</p> | <p></p>
`--network-mode` | <p>Set the network mode</p> | <p>string</p> | <p>no -> disables networking</p><p>basic -> enables networking only for cdh, mapr, hdp</p><p>all -> enables networking for cdh, mapr, hdp, as well as for Presto, PostgreSQL and Kerberos</p> | <p></p>
`--auto-install` | <p>Auto-install mode for Hadoop that enables Zookeeper</p> | <p>-</p> | <p>-</p> | <p></p>
`--manual-install` | <p>Run containers without AtScale installed</p> | <p>-</p> | <p>-</p> | <p></p>
`--container-group, -cg` | <p>Container group to use for the containers</p> | <p>string</p> | <p>-</p> | <p></p>
`--container-group-filename` | <p>Choose a custom path to a file to keep data for the container group</p> | <p>string -> path to file</p> | <p>-</p> | <p></p>
<b>AtScale params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--engine-memory` | <p>Memory, in megabytes, available to AtScale</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--license, -l` | <p>License file location for AtScale</p> | <p>string -> path to file</p> | <p>-</p> | <p></p>
`--platform, -p` | <p>Platform name for the data warehouse</p><p>This parameter can be optionally indexed for independence (ex: --platform1)</p> | <p>string</p> | <p>cdp, cdh, hdp, mapr, bigquery, redshift, snowflake, postgres, presto, oracle, db2, mssql, other, universal, databricks, databrickssql, synapse, iris, livy, salesforce, starburst</p> | <p></p>
`--platform-version, -pv` | <p>Version for the data warehouse platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-version1)</p><p>Valid only when --platform is cdh or hdp</p> | <p>string</p> | <p>-</p> | <p></p>
`--platform-outbound-security-query-roles, -posqr` | <p>Sets query roles for the platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-outbound-security-query-roles1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--platform-outbound-security, -pos` | <p>Sets security flags for the platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-outbound-security1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--platform-outbound-security-system, -poss` | <p>Sets system security flags for the platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-outbound-security-system1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--platform-outbound-security-canary, -posc` | <p>Enables canary for the platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-outbound-security-canary1)</p> | <p>-</p> | <p>-</p> | <p></p>
`--as-queryengine, -asqe` | <p>Enables 5 query engine nodes without configuring them</p> | <p>-</p> | <p>-</p> | <p></p>
`--as-queryengine--configured, -asqec` | <p>Enables 5 query engine nodes and configures them</p> | <p>-</p> | <p>-</p> | <p></p>
`--enable-impersonation, -imp` | <p>Enables impersonation in AtScale</p> | <p>-</p> | <p>-</p> | <p></p>
`--enable-datadash` | <p>Enables Datadash</p> | <p>-</p> | <p>-</p> | <p></p>
`--as-ha` | <p>Enables high availability mode</p> | <p>-</p> | <p>-</p> | <p></p>
`--atscale-sql-engine, -ase` | <p>Set the SQL engine that will be used for both batch and interactive queries</p><p>This parameter can be optionally indexed for independence (ex: --atscale-sql-engine1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--as-sql-interactive` | <p>The SQL engine that will be used for interactive queries</p><p>This parameter can be optionally indexed for independence (ex: --as-sql-interactive1)</p><p>Cannot be applied to snowflake and bigquery engines</p> | <p>string</p> | <p>spark, hive, as-spark, as-hive, cdh-impala</p> | <p></p>
`--as-sql-batch` | <p>The SQL engine that will be used for batch queries</p><p>This parameter can be optionally indexed for independence (ex: --as-sql-batch1)</p> | <p>string</p> | <p>spark, hive, as-spark, as-hive, cdh-impala</p> | <p></p>
`--atscale-version, -asv` | <p>Set the full AtScale version, including the build number (ex: 6.4.0.228)</p> | <p>string</p> | <p>-</p> | <p></p>
`--atscale-branch, -asb` | <p>Set the AtScale branch name (ex: r6.5.0)</p> | <p>string</p> | <p>-</p> | <p></p>
`--connector-type, -ct` | <p>Overrides the default connector type, when SQL engine is set to Hadoop</p> | <p>string</p> | <p>-</p> | <p></p>
`--atscale-branch, -asb` | <p>Set the AtScale branch name (ex: r6.5.0)</p> | <p>string</p> | <p>-</p> | <p></p>
`--engine-branch` | <p>Set the engine branch name (ex: r6.5.0)</p> | <p>string</p> | <p>-</p> | <p></p>
`--engine-version` | <p>Set the full engine version (ex: 6.5.0.123)</p> | <p>string</p> | <p>-</p> | <p></p>
`--modeler-branch` | <p>Set the modeler branch name (ex: r6.5.0)</p> | <p>string</p> | <p>-</p> | <p></p>
`--modeler-version` | <p>Set the full modeler version (ex: 6.5.0.123)</p> | <p>string</p> | <p>-</p> | <p></p>
`--parameterized-strings-enabled` | <p>Enables parametrized strings in the engine</p> | <p>-</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p>
`--virtualization-supervisor-memory` | <p>Memory, in megabytes, available to the AtScale virtualization supervisor</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--virtualization-supervisor-cores` | <p>CPU cores count available for AtScale virtualization supervisor</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--virtualization-worker-memory` | <p>Memory, in megabytes, available to the AtScale virtualization worker</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--virtualization-worker-cores` | <p>CPU cores count available for AtScale virtualization worker</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--virtualization-listener-memory` | <p>Memory, in megabytes, available to the AtScale virtualization listener</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--virtualization-listener-cores` | <p>CPU cores count available for AtScale virtualization listener</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--disable-jdbc-ssl` | <p>If this param is passed, all settings related to SSL for JDBC connections for any SQL engine that is running will be disabled</p> | <p>-</p> | <p>-</p> | <p></p>
`--appdb_timeout` | <p>Set the bootstrap.conf timeout (in seconds) in the engine</p> | <p>number</p> | <p>-</p> | <p>Change ends up in bootstrap.conf</p>
`--aggregates-tablecache-enabled, -aggte` | <p>Changes the aggregates.tableCache.enabled setting in the engine</p> | <p>string</p> | <p>-</p> | <p></p>
`--load-default-data, -ldd` | <p>Enables AtScale dataloader and loads sample data</p> | <p>-</p> | <p>-</p> | <p></p>
`--load-security-data, -lsd` | <p>Enables AtScale dataloader and loads sample security data</p> | <p>-</p> | <p>-</p> | <p></p>
`--dataloader-bundle, -dlb` | <p>Provide sample data bundle for the AtScale dataloader to use</p> | <p>string -> path to directory</p> | <p>-</p> | <p></p>
`--dataloader-schema, -dls` | <p>Provide schema for the provided bundle for the AtScale dataloader to use</p> | <p>string</p> | <p>-</p> | <p></p>
`--use-ad, -uad` | <p>Configures active directory through the configure-directory.sh.j2 script</p> | <p>-</p> | <p>-</p> | <p></p>
`--secured` | <p>Enables EngineTLS and Kerberos MIT</p> | <p>-</p> | <p>-</p> | <p></p>
`--as-dev-mode` | <p>If set to false, dev mode is disabled in atscale.yaml</p> | <p>bool</p> | <p>true</p><p>false</p> | <p>Change ends up in atscale.yaml</p>
`--upgrade-to-branch, -utb` | <p>Prepare AtScale upgrade tests for the specified branch name</p> | <p>string</p> | <p>-</p> | <p></p>
`--upgrade-to-version, -utv` | <p>Prepare AtScale upgrade tests for the specified version</p> | <p>string</p> | <p>-</p> | <p></p>
`--bigquery-credentials, -bq-cred` | <p>Optionally, the default credentials file applied during setup of BigQuery data warehouse can be overwritten using this parameter</p> | <p>string -> path to file</p> | <p>-</p> | <p></p>
`--bigquery-bucket, -bq-bucket` | <p>Optionally, the default bucket value of BigQuery can be overwritten using this parameter</p> | <p>string -> excluding ‘gs://’ prefix</p> | <p>-</p> | <p></p>
`--test-tag-p` | <p>(For testing purposes only) Set custom tag for platform images</p> | <p>string</p> | <p>-</p> | <p></p>
`--test-tag-a` | <p>(For testing purposes only) Set custom tag for AtScale images</p> | <p>string</p> | <p>-</p> | <p></p>
`--inbound-kerberos-ad, -ikrb-ad` | <p>Enables KerberosAD</p> | <p>-</p> | <p>-</p> | <p></p>
`--inbound-kerberos-mit, -ikrb-mit` | <p>Enables Kerberos MIT</p> | <p>-</p> | <p>-</p> | <p></p>
`--inbound-tls, -itls` | <p>Enables InboundTLS</p> | <p>-</p> | <p>-</p> | <p></p>
`--platform-outbound-partial-agg-hit, -popah` | <p>Enables partial agg hit for the platform</p><p>This parameter can be optionally indexed for independence (ex: --platform-outbound-partial-agg-hit1)</p> | <p>-</p> | <p>-</p> | <p></p>
`--engine-tls, -etls` | <p>Enables EngineTLS</p> | <p>-</p> | <p>-</p> | <p></p>
`--engine-setting, -eset` | <p>Additional setting/s for the engine</p><p>This parameter can be optionally indexed for independence (ex: --engine-setting1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--engine-settings-file, -esf` | <p>Path to file containing additional settings for the engine</p> | <p>string -> path to file</p> | <p>-</p> | <p></p>
`--vault` | <p>enabled vault integration with devops vault</p> | <p>-</p> | <p>-</p> | <p></p>
`--external-engine, ** Deprecated` | <p>utils/configure-external.sh script should be used to set external engine</p> | <p>-</p> | <p>-</p> | <p></p>
`--external-modeler, ** Deprecated` | <p>utils/configure-external.sh script should be used to set external modeler</p> | <p>-</p> | <p>-</p> | <p></p>
`--external-account, ** Deprecated` | <p>utils/configure-external.sh script should be used to set external account</p> | <p>-</p> | <p>-</p> | <p></p>
`--interactive-mode, ** Unknown usage` | <p>If provided it disables AtScale dataloader, but besides that I did not find any use</p> | <p>-</p> | <p>-</p> | <p></p>
<b>AtScale SaaS params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--infraapi-branch, -iab` | <p>Full branch name that will be used for the InfraAPI</p><p>Valid only when running run-atscale-saas.sh, instead of run-atscale.sh</p> | <p>string</p> | <p>-</p> | <p></p>
`--infraapi-version, -iav` | <p>Full version that will be used for the InfraAPI</p><p>Valid only when running run-atscale-saas.sh, instead of run-atscale.sh</p> | <p>string</p> | <p>-</p> | <p></p>
<b>AtScale virtualization cluster params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--as-virtualization-dev, -vdev` | <p>Activates default virtualization cluster</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION_DEV</p>
`--as-virtualization-jenkins` | <p>Activates virtualization cluster with 1 AtScale compute node</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION_JENKINS</p>
`--as-virtualization` | <p>Activates virtualization cluster with 5 AtScale compute nodes</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION</p>
`--as-virtualization-configured, -vconf` | <p>Activates virtualization cluster with 5 AtScale compute nodes</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION_CONF</p>
`--as-virtualization-large, -vlarge` | <p>Activates virtualization cluster with 12 AtScale compute nodes</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION_LARGE</p>
`--as-virtualization-large-configured, -vlargeconf` | <p>Activates virtualization cluster with 12 AtScale compute nodes</p> | <p>-</p> | <p>-</p> | <p>Env: $AS_VIRTUALIZATION_LARGE_CONF</p>
<b>Querytester params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--querytester-mode` | <p>Create a Querytester container</p> | <p>-</p> | <p>-</p> | <p>Env: $QUERYTESTER_MODE</p>
`--querytester-group, -qt-g` | <p>Querytester group</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_GROUP_ES</p>
`--querytester-suite, -qt-s` | <p>Querytester suite</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_SUITE_ES</p>
`--querytester-auth-user, -qt-u` | <p>Authentication user that will be used by Querytester</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_AUTH_USER</p>
`--querytester-auth-password, -qt-p` | <p>Password for the authentication user that will be used by Querytester</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_AUTH_PASSWORD</p>
`--querytester-branch, -qt-branch` | <p>Querytester branch name</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_BRANCH</p>
`--querytester-build, -qt-build` | <p>Querytester build number</p> | <p>string</p> | <p>-</p> | <p>Env: $QT_BUILD</p>
`--querytester-output, -qt-output` | <p>Output format from the Querytester</p> | <p>string</p> | <p>json</p><p>xml</p> | <p></p>
`--no-tests` | <p>Skip tests</p> | <p>-</p> | <p>-</p> | <p></p>
`--no-kill` | <p>Keep Querytester containers running after tests are completed</p> | <p>-</p> | <p>-</p> | <p></p>
<b>Nightwatch params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--nightwatch-restart-test-containers, -nwrtc` | <p>Removes Nightwatch, Selenium and Querytester containers from previous runs</p> | <p>-</p> | <p>-</p> | <p></p>
`--nightwatch-suite, -nws` | <p>File name with .js extension for Nightwatch suite</p> | <p>string</p> | <p>-</p> | <p></p>
`--nightwatch-view-port, -nwvp` | <p>Enables the Nightwatch view port (5900)</p> | <p>-</p> | <p>-</p> | <p></p>
`--nightwatch-modeler-path, -nwmp` | <p>Path to directory, containing modeler tests for Nightwatch</p> | <p>string -> path to directory</p> | <p>-</p> | <p></p>
`--nightwatch-load-default-data, -nwldd` | <p>Load sample data into Nightwatch</p> | <p>-</p> | <p>-</p> | <p></p>
`--nightwatch-load-security-data, -nwlsd` | <p>Load sample security data into Nightwatch</p> | <p>-</p> | <p>-</p> | <p></p>
`--no-data` | <p>Disables dataloader for Nightwatch and ignores sample data</p> | <p>-</p> | <p>-</p> | <p></p>
`--configure-for-ad, -cad` | <p>Configures active directory for Nightwatch through the configure-for-ad.sh script</p> | <p>-</p> | <p>-</p> | <p></p>
`--kerberized` | <p>Enables Kerberos in Nightwatch and Querytester containers</p> | <p>-</p> | <p>-</p> | <p></p>
`--infraapi-dnsfix, -iadns` | <p>Configures DNS configuration for Nightwatch in /modeler/nightwatch.conf.js</p> | <p>-</p> | <p>-</p> | <p>Change ends up in /modeler/nightwatch.conf.js</p>
`--nightwatch-default-schema, -nwds, ** Unknown usage` | <p>Unknown usage</p> | <p>string</p> | <p>-</p> | <p>Env: $NIGHTWATCH_DEFAULT_SCHEMA</p>
`--nightwatch-pre-upgrade-branch, -nwdup, ** Unknown usage` | <p>Unknown usage</p> | <p>string</p> | <p>-</p> | <p>Env: $NIGHTWATCH_PRE_UPGRADE_BRANCH</p>
<b>Hadoop params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--enable-kms` | <p>Enables KMS in Hadoop</p> | <p>-</p> | <p>-</p> | <p></p>
`--yarn-cpu` | <p>CPU cores count available for Yarn</p><p>Yarn is the resource management and job scheduling service in Hadoop</p> | <p>number</p> | <p>-</p> | <p>Env: $YARN_PARAMETERS</p><p>Used in set-hadoop-param.sh</p>
`--yarn-memory` | <p>Memory, in megabytes, available to Yarn</p> | <p>number</p> | <p>-</p> | <p>Env: $YARN_PARAMETERS</p><p>Used in set-hadoop-param.sh</p>
`--impala-memory` | <p>Memory, in megabytes, available to Impala</p><p>Impala is the SQL query engine for processing stored data in Hadoop</p> | <p>number</p> | <p></p> | <p>Env: $IMPALA_PARAMETERS</p><p>Used in set-hadoop-param.sh</p>
`--multiple-impalas` | <p>Indicates whether to use multiple impala instances for the SQL query engine</p> | <p>-</p> | <p>-</p> | <p>Env: $MULTIPLE_IMPALAS</p><p>Used in set-hadoop-param.sh</p>
`--tez-am-memory` | <p>Memory, in megabytes, available to Tez master</p> | <p>number</p> | <p>-</p> | <p>Env: $HIVE_PARAMETERS</p><p>Used in set-hadoop-param.sh</p><p>Change ends up in /etc/hive/conf/tez-site.xml</p>
`--tez-container-memory` | <p>Memory, in megabytes, available to each Tez container</p> | <p>number</p> | <p>-</p> | <p>Env: $HIVE_PARAMETERS</p><p>Used in set-hadoop-param.sh</p><p>Change ends up in /etc/hive/conf/tez-site.xml</p>
<b>Spark params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--spark-standalone, -sps` | <p>Set the version of Spark standalone</p><p>This parameter can be optionally indexed for independence (ex: --spark-standalone1)</p> | <p>string</p> | <p>-</p> | <p></p>
`--spark-driver-memory` | <p>Memory, in megabytes, available to the Spark driver</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_SPARK_PARAMETERS, $HIVE_PARAMETERS</p><p>Used in set-hadoop-param.sh</p><p>Change ends up in /etc/spark2/conf/spark-defaults.conf</p>
`--spark-executor-memory` | <p>Memory, in megabytes, available to each Spark executor instance</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_SPARK_PARAMETERS, $HIVE_PARAMETERS</p><p>Used in set-hadoop-param.sh</p><p>Change ends up in /etc/spark2/conf/spark-defaults.conf</p>
`--spark-executor-instances` | <p>Count for Spark executor nodes</p> | <p>number</p> | <p>-</p> | <p>Env: $ATSCALE_SPARK_PARAMETERS, $HIVE_PARAMETERS</p><p>Used in set-hadoop-param.sh</p><p>Change ends up in /etc/spark2/conf/spark-defaults.conf</p>
<b>Zookeeper params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--zookeeper-version, -zkv` | <p>Optionally, modify the Zookeeper version that will be used</p> | <p>string</p> | <p>-</p> | <p></p>
`--zookeeper-count, -zkc` | <p>Choose nodes count for Zookeeper</p> | <p>number</p> | <p>-</p> | <p></p>
<b>Docker mount params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--as-mount` | <p>Mount chosen local atscale directory into the atscale container in /data/mount</p> | <p>string -> path to an atscale directory</p> | <p>-</p> | <p>Env: $AS_MOUNT</p>
`--as-expose` | <p>Mount chosen local expose directory into the atscale container in /opt/atscale</p> | <p>string -> path to directory, containing an atscale expose directory</p> | <p>-</p> | <p>Env: $AS_EXPOSE</p>
`--hadoop-expose` | <p>Mount chosen local data directory into the hadoop container in /data</p> | <p>string -> path to directory, containing a hadoop data directory </p> | <p>-</p> | <p>Env: $HADOOP_EXPOSE</p>
`--keep-state` | <p>Expose both /opt/atscale and /data without overwriting directory state</p> | <p>string -> path to directory</p> | <p>-</p> | <p>Env: $KEEP_STATE</p>
<b>Logging params</b>
Parameter alias | Description | Expected value | Choices | Code remarks
--- | --- | --- | --- | ---
`--debug` | <p>Shows additional info from created docker objects like containers, volumes and networks</p> | <p>-</p> | <p>-</p> | <p></p>
`--gather-diagnostic, --querytester-diagnostic, -diag, -qt-diag` | <p>Collects and zips logs and debug information from all containers, including Querytester and Nightwatch ones</p> | <p>string</p> | <p>local -> exports results in /tmp/</p><p>basic -> uploads results in s3://docker-container-logs.atscale.com</p><p>upload -> same as basic</p> | <p></p>
`--log-to-es` | <p>Enables logging to Elasticsearch</p> | <p>-</p> | <p>-</p> | <p></p>
`--logstash-log-destination` | <p>If logging to Elasticsearch is enabled, Logstash log destination should be defined here</p> | <p>string</p> | <p>-</p> | <p></p>
`--logstash-metric-destination` | <p>If logging to Elasticsearch is enabled, Logstash metrics destination should be defined here</p> | <p>string</p> | <p>-</p> | <p></p>
`--as-logging-dev` | <p>Enables Logging Infra services</p> | <p>-</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--as-governance-dev` | <p>Enables Governance services</p> | <p>-</p> | <p>-</p> | <p>Env: $ATSCALE_PARAMETERS</p><p>Used in set-atscale-param.sh</p><p>Change ends up in atscale.yaml</p>
`--cct-version, -cctv, ** Unknown usage` | <p>Unknown usage</p> | <p>string</p> | <p>-</p> | <p></p>
`--count-containers, -cc, ** Unknown usage` | <p>Unknown usage</p> | <p>-</p> | <p>-</p> | <p></p>
