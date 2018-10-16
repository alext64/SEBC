Create my user: 

```shell
sudo useradd -m alext64
```

... and my hdfs home: 

```
hadoop fs -mkdir /user/alext64/
```

authorizing: 

```shell
hadoop fs -chown alext64:alext64 /user/alext64/
```

```
sudo su - alext64

export HADOOP_USER_NAME=alext64
```

Running teragen:

```shell
 time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=33554432 104857600  /user/alext64/unsorted1 2>&1 | tee teragen$(date +'%Y%m%d%H%M%S')

18/10/16 12:22:34 INFO mapreduce.Job: Job job_local1382877698_0001 completed successfully
18/10/16 12:22:34 INFO mapreduce.Job: Counters: 21
        File System Counters
                FILE: Number of bytes read=276519
                FILE: Number of bytes written=621444
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=0
                HDFS: Number of bytes written=10485760000
                HDFS: Number of read operations=4
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Map-Reduce Framework
                Map input records=104857600
                Map output records=104857600
                Input split bytes=83
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1304
                Total committed heap usage (bytes)=157286400
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=225186913807133164
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10485760000

real    4m31.046s
user    4m46.921s
sys     0m22.643s

```

and terasort:

```shell
 time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar terasort  /user/alext64/unsorted1 /user/alext64/sorted1 2>&1 | tee teragen$(date +'%Y%m%d%H%M%S'
 
18/10/16 13:03:43 INFO mapreduce.Job: Job job_1539694319565_0001 completed successfully
18/10/16 13:03:43 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4689929658
                FILE: Number of bytes written=9325889988
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10485797247
                HDFS: Number of bytes written=10485760000
                HDFS: Number of read operations=975
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=313
                Launched reduce tasks=12
                Data-local map tasks=313
                Total time spent by all maps in occupied slots (ms)=3187072
                Total time spent by all reduces in occupied slots (ms)=1184377
                Total time spent by all map tasks (ms)=3187072
                Total time spent by all reduce tasks (ms)=1184377
                Total vcore-milliseconds taken by all map tasks=3187072
                Total vcore-milliseconds taken by all reduce tasks=1184377
                Total megabyte-milliseconds taken by all map tasks=3263561728
                Total megabyte-milliseconds taken by all reduce tasks=1212802048
        Map-Reduce Framework
                Map input records=104857600
                Map output records=104857600
                Map output bytes=10695475200
                Map output materialized bytes=4587419213
                Input split bytes=37247
                Combine input records=0
                Combine output records=0
                Reduce input groups=104857600
                Reduce shuffle bytes=4587419213
                Reduce input records=104857600
                Reduce output records=104857600
                Spilled Records=209715200
                Shuffled Maps =3756
                Failed Shuffles=0
                Merged Map outputs=3756
                GC time elapsed (ms)=104958
                CPU time spent (ms)=2875520
                Physical memory (bytes) snapshot=168888279040
                Virtual memory (bytes) snapshot=909379665920
                Total committed heap usage (bytes)=174112374784
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10485760000
        File Output Format Counters
                Bytes Written=10485760000
18/10/16 13:03:43 INFO terasort.TeraSort: done

real    8m12.316s
user    0m19.572s
sys     0m2.420s

```

