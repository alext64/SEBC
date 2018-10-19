```
kinit raffles@ALEXT64.SG

time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/raffles/tgen512/* /user/raffles/tgen512m
```

```SHELL
18/10/19 11:20:46 INFO terasort.TeraSort: starting
18/10/19 11:20:50 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539948049972, maxDate=1540552849972, sequenceNumber=9, masterKeyId=4 on 10.0.0.4:8020
18/10/19 11:20:50 INFO security.TokenCache: Got dt for hdfs://sebx01.westeurope.cloudapp.azure.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539948049972, maxDate=1540552849972, sequenceNumber=9, masterKeyId=4)
18/10/19 11:20:50 INFO input.FileInputFormat: Total input paths to process : 6
Spent 922ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 925ms
Sampling 10 splits of 156
Making 16 from 100000 sampled records
Computing parititions took 1094ms
Spent 2021ms computing partitions.
18/10/19 11:20:51 INFO client.RMProxy: Connecting to ResourceManager at sebx01.westeurope.cloudapp.azure.com/10.0.0.4:8032
18/10/19 11:20:52 INFO mapreduce.JobSubmitter: number of splits:156
18/10/19 11:20:52 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539947756376_0002
18/10/19 11:20:52 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.4:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@ALEXT64.SG, renewer=yarn, realUser=, issueDate=1539948049972, maxDate=1540552849972, sequenceNumber=9, masterKeyId=4)
18/10/19 11:20:53 INFO impl.YarnClientImpl: Submitted application application_1539947756376_0002
18/10/19 11:20:53 INFO mapreduce.Job: The url to track the job: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_1539947756376_0002/
18/10/19 11:20:53 INFO mapreduce.Job: Running job: job_1539947756376_0002
18/10/19 11:21:10 INFO mapreduce.Job: Job job_1539947756376_0002 running in uber mode : false
18/10/19 11:21:10 INFO mapreduce.Job:  map 0% reduce 0%
18/10/19 11:21:23 INFO mapreduce.Job:  map 1% reduce 0%
18/10/19 11:21:24 INFO mapreduce.Job:  map 2% reduce 0%
18/10/19 11:21:32 INFO mapreduce.Job:  map 4% reduce 0%
18/10/19 11:21:34 INFO mapreduce.Job:  map 6% reduce 0%
18/10/19 11:21:35 INFO mapreduce.Job:  map 13% reduce 0%
18/10/19 11:21:45 INFO mapreduce.Job:  map 15% reduce 0%
18/10/19 11:21:46 INFO mapreduce.Job:  map 17% reduce 0%
18/10/19 11:21:49 INFO mapreduce.Job:  map 20% reduce 0%
18/10/19 11:21:50 INFO mapreduce.Job:  map 22% reduce 0%
18/10/19 11:21:51 INFO mapreduce.Job:  map 24% reduce 0%
18/10/19 11:21:56 INFO mapreduce.Job:  map 25% reduce 0%
18/10/19 11:21:57 INFO mapreduce.Job:  map 26% reduce 0%
18/10/19 11:21:58 INFO mapreduce.Job:  map 28% reduce 0%
18/10/19 11:22:01 INFO mapreduce.Job:  map 29% reduce 0%
18/10/19 11:22:03 INFO mapreduce.Job:  map 31% reduce 0%
18/10/19 11:22:04 INFO mapreduce.Job:  map 35% reduce 0%
18/10/19 11:22:07 INFO mapreduce.Job:  map 36% reduce 0%
18/10/19 11:22:08 INFO mapreduce.Job:  map 37% reduce 0%
18/10/19 11:22:11 INFO mapreduce.Job:  map 38% reduce 0%
18/10/19 11:22:12 INFO mapreduce.Job:  map 39% reduce 0%
18/10/19 11:22:14 INFO mapreduce.Job:  map 40% reduce 0%
18/10/19 11:22:16 INFO mapreduce.Job:  map 42% reduce 0%
18/10/19 11:22:17 INFO mapreduce.Job:  map 43% reduce 0%
18/10/19 11:22:18 INFO mapreduce.Job:  map 46% reduce 0%
18/10/19 11:22:19 INFO mapreduce.Job:  map 47% reduce 0%
18/10/19 11:22:20 INFO mapreduce.Job:  map 48% reduce 0%
18/10/19 11:22:24 INFO mapreduce.Job:  map 50% reduce 0%
18/10/19 11:22:27 INFO mapreduce.Job:  map 51% reduce 0%
18/10/19 11:22:28 INFO mapreduce.Job:  map 52% reduce 0%
18/10/19 11:22:30 INFO mapreduce.Job:  map 54% reduce 0%
18/10/19 11:22:31 INFO mapreduce.Job:  map 55% reduce 0%
18/10/19 11:22:32 INFO mapreduce.Job:  map 58% reduce 0%
18/10/19 11:22:37 INFO mapreduce.Job:  map 61% reduce 0%
18/10/19 11:22:39 INFO mapreduce.Job:  map 62% reduce 0%
18/10/19 11:22:40 INFO mapreduce.Job:  map 63% reduce 0%
18/10/19 11:22:43 INFO mapreduce.Job:  map 64% reduce 0%
18/10/19 11:22:44 INFO mapreduce.Job:  map 65% reduce 0%
18/10/19 11:22:45 INFO mapreduce.Job:  map 67% reduce 0%
18/10/19 11:22:46 INFO mapreduce.Job:  map 68% reduce 0%
18/10/19 11:22:47 INFO mapreduce.Job:  map 69% reduce 0%
18/10/19 11:22:57 INFO mapreduce.Job:  map 70% reduce 0%
18/10/19 11:23:00 INFO mapreduce.Job:  map 71% reduce 0%
18/10/19 11:23:03 INFO mapreduce.Job:  map 72% reduce 0%
18/10/19 11:23:07 INFO mapreduce.Job:  map 73% reduce 0%
18/10/19 11:23:09 INFO mapreduce.Job:  map 74% reduce 0%
18/10/19 11:23:14 INFO mapreduce.Job:  map 77% reduce 0%
18/10/19 11:23:15 INFO mapreduce.Job:  map 78% reduce 0%
18/10/19 11:23:19 INFO mapreduce.Job:  map 79% reduce 0%
18/10/19 11:23:21 INFO mapreduce.Job:  map 80% reduce 0%
18/10/19 11:23:25 INFO mapreduce.Job:  map 82% reduce 0%
18/10/19 11:23:28 INFO mapreduce.Job:  map 83% reduce 0%
18/10/19 11:23:31 INFO mapreduce.Job:  map 84% reduce 0%
18/10/19 11:23:34 INFO mapreduce.Job:  map 85% reduce 0%
18/10/19 11:23:36 INFO mapreduce.Job:  map 87% reduce 0%
18/10/19 11:23:37 INFO mapreduce.Job:  map 88% reduce 0%
18/10/19 11:23:42 INFO mapreduce.Job:  map 90% reduce 0%
18/10/19 11:23:46 INFO mapreduce.Job:  map 90% reduce 2%
18/10/19 11:23:48 INFO mapreduce.Job:  map 92% reduce 2%
18/10/19 11:23:49 INFO mapreduce.Job:  map 93% reduce 4%
18/10/19 11:23:52 INFO mapreduce.Job:  map 94% reduce 4%
18/10/19 11:23:53 INFO mapreduce.Job:  map 94% reduce 6%
18/10/19 11:23:54 INFO mapreduce.Job:  map 95% reduce 6%
18/10/19 11:23:55 INFO mapreduce.Job:  map 96% reduce 6%
18/10/19 11:23:57 INFO mapreduce.Job:  map 97% reduce 14%
18/10/19 11:23:59 INFO mapreduce.Job:  map 98% reduce 16%
18/10/19 11:24:01 INFO mapreduce.Job:  map 99% reduce 16%
18/10/19 11:24:06 INFO mapreduce.Job:  map 100% reduce 16%
18/10/19 11:24:08 INFO mapreduce.Job:  map 100% reduce 19%
18/10/19 11:24:09 INFO mapreduce.Job:  map 100% reduce 22%
18/10/19 11:24:10 INFO mapreduce.Job:  map 100% reduce 23%
18/10/19 11:24:11 INFO mapreduce.Job:  map 100% reduce 26%
18/10/19 11:24:14 INFO mapreduce.Job:  map 100% reduce 33%
18/10/19 11:24:15 INFO mapreduce.Job:  map 100% reduce 43%
18/10/19 11:24:16 INFO mapreduce.Job:  map 100% reduce 44%
18/10/19 11:24:17 INFO mapreduce.Job:  map 100% reduce 55%
18/10/19 11:24:20 INFO mapreduce.Job:  map 100% reduce 67%
18/10/19 11:24:21 INFO mapreduce.Job:  map 100% reduce 73%
18/10/19 11:24:22 INFO mapreduce.Job:  map 100% reduce 76%
18/10/19 11:24:23 INFO mapreduce.Job:  map 100% reduce 86%
18/10/19 11:24:24 INFO mapreduce.Job:  map 100% reduce 87%
18/10/19 11:24:25 INFO mapreduce.Job:  map 100% reduce 88%
18/10/19 11:24:26 INFO mapreduce.Job:  map 100% reduce 95%
18/10/19 11:24:27 INFO mapreduce.Job:  map 100% reduce 96%
18/10/19 11:24:29 INFO mapreduce.Job:  map 100% reduce 98%
18/10/19 11:24:30 INFO mapreduce.Job:  map 100% reduce 99%
18/10/19 11:24:32 INFO mapreduce.Job:  map 100% reduce 100%
18/10/19 11:24:33 INFO mapreduce.Job: Job job_1539947756376_0002 completed successfully
18/10/19 11:24:33 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2283991788
                FILE: Number of bytes written=4550377003
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120022932
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=516
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=32
        Job Counters
                Launched map tasks=156
                Launched reduce tasks=16
                Data-local map tasks=156
                Total time spent by all maps in occupied slots (ms)=2132955
                Total time spent by all reduces in occupied slots (ms)=626635
                Total time spent by all map tasks (ms)=2132955
                Total time spent by all reduce tasks (ms)=626635
                Total vcore-milliseconds taken by all map tasks=2132955
                Total vcore-milliseconds taken by all reduce tasks=626635
                Total megabyte-milliseconds taken by all map tasks=2184145920
                Total megabyte-milliseconds taken by all reduce tasks=641674240
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2240169991
                Input split bytes=22932
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2240169991
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =2496
                Failed Shuffles=0
                Merged Map outputs=2496
                GC time elapsed (ms)=65075
                CPU time spent (ms)=1581700
                Physical memory (bytes) snapshot=92023775232
                Virtual memory (bytes) snapshot=481405698048
                Total committed heap usage (bytes)=96360988672
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
18/10/19 11:24:33 INFO terasort.TeraSort: done

real    3m49.084s
user    0m17.749s
sys     0m2.917s

```

