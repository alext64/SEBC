*The teragen command*

```shell
[alext@sebx02 ~]$ sudo -E su - raffles

[raffles@sebx02 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapreduce.job.maps=6 -Ddfs.block.size=33554432 51200000 /user/raffles/tgen512
```

*The time command output*

```shell
real    1m25.143s
user    0m14.016s
sys     0m2.039s
```

*The output comman of hdfs dfs -ls /user/raffles/tgen512*

```
Found 7 items
-rw-r--r--   3 raffles raffles          0 2018-10-19 09:33 /user/raffles/tgen512/_SUCCESS
-rw-r--r--   3 raffles raffles  853333400 2018-10-19 09:32 /user/raffles/tgen512/part-m-00000
-rw-r--r--   3 raffles raffles  853333300 2018-10-19 09:32 /user/raffles/tgen512/part-m-00001
-rw-r--r--   3 raffles raffles  853333300 2018-10-19 09:32 /user/raffles/tgen512/part-m-00002
-rw-r--r--   3 raffles raffles  853333400 2018-10-19 09:32 /user/raffles/tgen512/part-m-00003
-rw-r--r--   3 raffles raffles  853333300 2018-10-19 09:32 /user/raffles/tgen512/part-m-00004
-rw-r--r--   3 raffles raffles  853333300 2018-10-19 09:33 /user/raffles/tgen512/part-m-00005
```

*How many blocks are associated with this directory*

```shel
[alext@sebx01 ~]$ hdfs fsck -blocks /user/raffles/tgen512

Connecting to namenode via http://sebx01.westeurope.cloudapp.azure.com:50070/fsck?ugi=alext&blocks=1&path=%2Fuser%2Fraffles%2Ftgen512
FSCK started by alext (auth:SIMPLE) from /10.0.0.4 for path /user/raffles/tgen512 at Fri Oct 19 09:38:37 UTC 2018
.......Status: HEALTHY
 Total size:    5120000000 B
 Total dirs:    1
 Total files:   7
 Total symlinks:                0
 Total blocks (validated):      156 (avg. block size 32820512 B)
 Minimally replicated blocks:   156 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Oct 19 09:38:37 UTC 2018 in 6 milliseconds


The filesystem under path '/user/raffles/tgen512' is HEALTHY
```

