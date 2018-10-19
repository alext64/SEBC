```shell
[raffles@sebx01 ~]$ kinit fullerton@ALEXT64.SG
Password for fullerton@ALEXT64.SG:
kinit: Password incorrect while getting initial credentials
[raffles@sebx01 ~]$ kinit fullerton@ALEXT64.SG
Password for fullerton@ALEXT64.SG:


```

```shell
[raffles@sebx01 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar pi 10 10000
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
18/10/19 10:25:13 INFO client.RMProxy: Connecting to ResourceManager at sebx01.westeurope.cloudapp.azure.com/10.0.0.4:8032
18/10/19 10:25:14 INFO input.FileInputFormat: Total input paths to process : 10
18/10/19 10:25:14 INFO mapreduce.JobSubmitter: number of splits:10
18/10/19 10:25:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1539940648371_0004
18/10/19 10:25:15 INFO impl.YarnClientImpl: Submitted application application_1539940648371_0004
18/10/19 10:25:15 INFO mapreduce.Job: The url to track the job: http://sebx01.westeurope.cloudapp.azure.com:8088/proxy/application_1539940648371_0004/
18/10/19 10:25:15 INFO mapreduce.Job: Running job: job_1539940648371_0004
18/10/19 10:25:27 INFO mapreduce.Job: Job job_1539940648371_0004 running in uber mode : false
18/10/19 10:25:27 INFO mapreduce.Job:  map 0% reduce 0%
18/10/19 10:25:36 INFO mapreduce.Job:  map 80% reduce 0%
18/10/19 10:25:37 INFO mapreduce.Job:  map 100% reduce 0%
18/10/19 10:25:46 INFO mapreduce.Job:  map 100% reduce 100%
18/10/19 10:25:46 INFO mapreduce.Job: Job job_1539940648371_0004 completed successfully
18/10/19 10:25:46 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=109
                FILE: Number of bytes written=1656509
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2940
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=70433
                Total time spent by all reduces in occupied slots (ms)=6803
                Total time spent by all map tasks (ms)=70433
                Total time spent by all reduce tasks (ms)=6803
                Total vcore-milliseconds taken by all map tasks=70433
                Total vcore-milliseconds taken by all reduce tasks=6803
                Total megabyte-milliseconds taken by all map tasks=72123392
                Total megabyte-milliseconds taken by all reduce tasks=6966272
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=350
                Input split bytes=1760
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
                GC time elapsed (ms)=1984
                CPU time spent (ms)=17710
                Physical memory (bytes) snapshot=4847980544
                Virtual memory (bytes) snapshot=30765047808
                Total committed heap usage (bytes)=5110759424
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
Job Finished in 34.039 seconds
Estimated value of Pi is 3.14120000000000000000

```

