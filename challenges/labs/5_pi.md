```shell
[raffles@sebx01 ~]$ kinit fullerton@ALEXT64.SG
Password for fullerton@ALEXT64.SG:
kinit: Password incorrect while getting initial credentials
[raffles@sebx01 ~]$ kinit fullerton@ALEXT64.SG
Password for fullerton@ALEXT64.SG:


```

```shell
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 10 10000
Number of Maps  = 10
Samples per Map = 10000
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
18/10/19 11:22:10 INFO client.RMProxy: Connecting to ResourceManager at sebx01.westeurope.cloudapp.azure.com/10.0.0.4:8032
18/10/19 11:22:11 INFO hdfs.DFSClient: Created token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@ALEXT64.SG, renewer=yarn, realUser=,                                               issueDate=1539948131184, maxDate=1540552931184, sequenceNumber=10, masterKeyId=4 on 10.0.0.4:8020
18/10/19 11:22:11 INFO security.TokenCache: Got dt for hdfs://sebx01.westeurope.cloudapp.azure.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service:                                               10.0.0.4:8020, Ident: (token for fullerton: HDFS_DELEGATION_TOKEN owner=fullerton@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539948131184,                                               maxDate=1540552931184, sequenceNumber=10, masterKeyId=4)
18/10/19 11:22:11 INFO input.FileInputFormat: Total input paths to process : 10
18/10/19 11:22:12 INFO mapreduce.JobSubmitter: number of splits:10
18/10/19 11:22:12 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539947756376_0003
18/10/19 11:22:12 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for fullerton: HDFS_DELEGATIO                                              N_TOKEN owner=fullerton@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539948131184, maxDate=1540552931184, sequenceNumber=10, masterKeyId=4)
18/10/19 11:22:13 INFO impl.YarnClientImpl: Submitted application application_1539947756376_0003
18/10/19 11:22:13 INFO mapreduce.Job: The url to track the job: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_153994775637                                              6_0003/
18/10/19 11:22:13 INFO mapreduce.Job: Running job: job_1539947756376_0003
18/10/19 11:22:40 INFO mapreduce.Job: Job job_1539947756376_0003 running in uber mode : false
18/10/19 11:22:40 INFO mapreduce.Job:  map 0% reduce 0%
18/10/19 11:22:51 INFO mapreduce.Job:  map 10% reduce 0%
18/10/19 11:22:53 INFO mapreduce.Job:  map 20% reduce 0%
18/10/19 11:22:54 INFO mapreduce.Job:  map 40% reduce 0%
18/10/19 11:22:55 INFO mapreduce.Job:  map 50% reduce 0%
18/10/19 11:23:02 INFO mapreduce.Job:  map 70% reduce 0%
18/10/19 11:23:03 INFO mapreduce.Job:  map 90% reduce 0%
18/10/19 11:23:23 INFO mapreduce.Job:  map 90% reduce 30%
18/10/19 11:23:36 INFO mapreduce.Job:  map 100% reduce 30%
18/10/19 11:23:37 INFO mapreduce.Job:  map 100% reduce 100%
18/10/19 11:23:38 INFO mapreduce.Job: Job job_1539947756376_0003 completed successfully
18/10/19 11:23:38 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=110
                FILE: Number of bytes written=1666091
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2950
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=154150
                Total time spent by all reduces in occupied slots (ms)=31780
                Total time spent by all map tasks (ms)=154150
                Total time spent by all reduce tasks (ms)=31780
                Total vcore-milliseconds taken by all map tasks=154150
                Total vcore-milliseconds taken by all reduce tasks=31780
                Total megabyte-milliseconds taken by all map tasks=157849600
                Total megabyte-milliseconds taken by all reduce tasks=32542720
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=350
                Input split bytes=1770
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=350
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=2379
                CPU time spent (ms)=18420
                Physical memory (bytes) snapshot=5038678016
                Virtual memory (bytes) snapshot=30758313984
                Total committed heap usage (bytes)=5308940288
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 88.047 seconds
Estimated value of Pi is 3.14120000000000000000

```

