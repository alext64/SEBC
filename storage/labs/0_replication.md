*Acquire hdfs user rights:* export HADOOP_USER_NAME=hdfs

*Create my target directory :* hadoop fs -mkdir /user/alext64/

*Create my partner directory*: hadoop fs -mkdir /user/bdany70/

*Create a 500 MB file*: hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-examples.jar teragen -Dmapred.map.tasks=1 5242880 /user/alext64/unsorted 2>&1 | tee teragen_$(date +'%Y%m%d_%H%M%S')

*Take my partner file*: hadoop distcp  hdfs://elephant1.westeurope.cloudapp.azure.com:8020/user/bdany70/unsorted/part-m-00000 hdfs://sebc01:8020/user/bdany70/

There is a problem with our network configuration. **Investigating ....**

hadoop distcp hdfs://gianbo01.northeurope.cloudapp.azure.com/hdfs_lab/gianfolo/unsorted/part-m-00000 hdfs://sebc01:8020/user/bdany70/