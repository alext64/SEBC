```shell
[alext@sebx04 ~]$ kinit raffles@ALEXT64.SG
Password for raffles@ALEXT64.SG:
[alext@sebx04 ~]$ klist -l
Principal name                 Cache name
--------------                 ----------
raffles@ALEXT64.SG             FILE:/tmp/krb5cc_500
```



```shell


[alext@sebx04 ~]$ spark2-submit --class org.apache.spark.examples.SparkPi --master yarn --deploy-mode cluster /opt/cloudera/parcels/SPARK2-2.3.0.cloudera4-1.cdh5.13.3.p0.611179/lib/spark2/examples/jars/spark-examples_2.11-2.3.0.cloudera4.jar 10

18/10/19 21:39:31 INFO client.RMProxy: Connecting to ResourceManager at sebx01.westeurope.cloudapp.azure.com/10.0.0.4:8032
18/10/19 21:39:31 INFO yarn.Client: Requesting a new application from cluster with 4 NodeManagers
18/10/19 21:39:32 INFO yarn.Client: Verifying our application has not requested more than the maximum memory capability of the cluster (6093 MB per container)
18/10/19 21:39:32 INFO yarn.Client: Will allocate AM container, with 1408 MB memory including 384 MB overhead
18/10/19 21:39:32 INFO yarn.Client: Setting up container launch context for our AM
18/10/19 21:39:32 INFO yarn.Client: Setting up the launch environment for our AM container
18/10/19 21:39:32 INFO yarn.Client: Preparing resources for our AM container
18/10/19 21:39:32 INFO yarn.Client: Uploading resource file:/opt/cloudera/parcels/SPARK2-2.3.0.cloudera4-1.cdh5.13.3.p0.611179/lib/spark2/examples/jars/spark-examples_2.11-2.3.0.cloudera4.jar -> hdfs://sebx01.westeurope.cloudapp.azure.com:8020/user/raffles/.sparkStaging/application_1539947756376_0011/spark-examples_2.11-2.3.0.cloudera4.jar
18/10/19 21:39:33 INFO yarn.Client: Uploading resource file:/tmp/spark-e3068e0b-004e-4038-bcf8-b0f238a5433f/__spark_conf__6083150744902171822.zip -> hdfs://sebx01.westeurope.cloudapp.azure.com:8020/user/raffles/.sparkStaging/application_1539947756376_0011/__spark_conf__.zip
18/10/19 21:39:34 INFO spark.SecurityManager: Changing view acls to: alext,raffles
18/10/19 21:39:34 INFO spark.SecurityManager: Changing modify acls to: alext,raffles
18/10/19 21:39:34 INFO spark.SecurityManager: Changing view acls groups to:
18/10/19 21:39:34 INFO spark.SecurityManager: Changing modify acls groups to:
18/10/19 21:39:34 INFO spark.SecurityManager: SecurityManager: authentication disabled; ui acls disabled; users  with view permissions: Set(alext, raffles); groups with view permissions: Set(); users  with modify permissions: Set(alext, raffles); groups with modify permissions: Set()
18/10/19 21:39:34 INFO security.HadoopFSDelegationTokenProvider: getting token for: DFS[DFSClient[clientName=DFSClient_NONMAPREDUCE_-1792935475_1, ugi=raffles@ALEXT64.SG (auth:KERBEROS)]]
18/10/19 21:39:34 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539985174289, maxDate=1540589974289, sequenceNumber=13, masterKeyId=4 on 10.0.0.4:8020
18/10/19 21:39:34 INFO security.HadoopFSDelegationTokenProvider: getting token for: DFS[DFSClient[clientName=DFSClient_NONMAPREDUCE_-1792935475_1, ugi=raffles@ALEXT64.SG (auth:KERBEROS)]]
18/10/19 21:39:35 INFO hive.metastore: Trying to connect to metastore with URI thrift://sebx01.westeurope.cloudapp.azure.com:9083
18/10/19 21:39:36 INFO hive.metastore: Opened a connection to metastore, current connections: 1
18/10/19 21:39:36 INFO hive.metastore: Connected to metastore.
18/10/19 21:39:36 INFO hive.metastore: Closed a connection to metastore, current connections: 0
18/10/19 21:39:39 INFO yarn.Client: Submitting application application_1539947756376_0011 to ResourceManager
18/10/19 21:39:39 INFO impl.YarnClientImpl: Submitted application application_1539947756376_0011
18/10/19 21:39:40 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:40 INFO yarn.Client:
         client token: Token { kind: YARN_CLIENT_TOKEN, service:  }
         diagnostics: N/A
         ApplicationMaster host: N/A
         ApplicationMaster RPC port: -1
         queue: root.users.raffles
         start time: 1539985179605
         final status: UNDEFINED
         tracking URL: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_1539947756376_0011/
         user: raffles
18/10/19 21:39:41 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:42 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:43 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:44 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:45 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:46 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:47 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:48 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:49 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:50 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:51 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:52 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:53 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:54 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:55 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:56 INFO yarn.Client: Application report for application_1539947756376_0011 (state: ACCEPTED)
18/10/19 21:39:57 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:39:57 INFO yarn.Client:
         client token: Token { kind: YARN_CLIENT_TOKEN, service:  }
         diagnostics: N/A
         ApplicationMaster host: 10.0.0.8
         ApplicationMaster RPC port: 0
         queue: root.users.raffles
         start time: 1539985179605
         final status: UNDEFINED
         tracking URL: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_1539947756376_0011/
         user: raffles
18/10/19 21:39:58 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:39:59 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:00 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:01 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:02 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:03 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:04 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:05 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:06 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:07 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:08 INFO yarn.Client: Application report for application_1539947756376_0011 (state: RUNNING)
18/10/19 21:40:09 INFO yarn.Client: Application report for application_1539947756376_0011 (state: FINISHED)
18/10/19 21:40:09 INFO yarn.Client:
         client token: N/A
         diagnostics: N/A
         ApplicationMaster host: 10.0.0.8
         ApplicationMaster RPC port: 0
         queue: root.users.raffles
         start time: 1539985179605
         final status: SUCCEEDED
         tracking URL: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_1539947756376_0011/
         user: raffles
18/10/19 21:40:10 INFO util.ShutdownHookManager: Shutdown hook called
18/10/19 21:40:10 INFO util.ShutdownHookManager: Deleting directory /tmp/spark-e3068e0b-004e-4038-bcf8-b0f238a5433f
18/10/19 21:40:10 INFO util.ShutdownHookManager: Deleting directory /tmp/spark-4fe21992-d7c7-48eb-a4da-ef11a4c66515

```

