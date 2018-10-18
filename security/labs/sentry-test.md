### Verify user privileges

```shell
[alext@sebc02 ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.13.3 by Apache Hive
beeline> !connect jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
scan complete in 6ms
Connecting to jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.13.3)
Driver: Hive JDBC (version 1.1.0-cdh5.13.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20181018004848_3afb11f1-06bb-4ed7-b899-b81ff6973b64): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018004848_3afb11f1-06bb-4ed7-b899-b81ff6973b64); Time taken: 1.924 seconds
INFO  : Executing command(queryId=hive_20181018004848_3afb11f1-06bb-4ed7-b899-b81ff6973b64): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018004848_3afb11f1-06bb-4ed7-b899-b81ff6973b64); Time taken: 1.029 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (4.821 seconds)
```

### Create a Sentry role with full authorization

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20181018004848_217920d0-0d11-4633-83dc-c75929f1c98e): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018004848_217920d0-0d11-4633-83dc-c75929f1c98e); Time taken: 0.156 seconds
INFO  : Executing command(queryId=hive_20181018004848_217920d0-0d11-4633-83dc-c75929f1c98e): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018004848_217920d0-0d11-4633-83dc-c75929f1c98e); Time taken: 0.314 seconds
INFO  : OK
No rows affected (0.496 seconds)
```

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20181018005151_1acdd027-3be1-4dcd-b545-00f7fa0022e1): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018005151_1acdd027-3be1-4dcd-b545-00f7fa0022e1); Time taken: 0.207 seconds
INFO  : Executing command(queryId=hive_20181018005151_1acdd027-3be1-4dcd-b545-00f7fa0022e1): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018005151_1acdd027-3be1-4dcd-b545-00f7fa0022e1); Time taken: 0.175 seconds
INFO  : OK
No rows affected (0.394 seconds)

```

```
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT ROLE sentry_admin TO GROUP alext64;
INFO  : Compiling command(queryId=hive_20181018005353_39d090d2-26b7-46f7-9232-f4cea2f29514): GRANT ROLE sentry_admin TO GROUP alext64
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018005353_39d090d2-26b7-46f7-9232-f4cea2f29514); Time taken: 0.249 seconds
INFO  : Executing command(queryId=hive_20181018005353_39d090d2-26b7-46f7-9232-f4cea2f29514): GRANT ROLE sentry_admin TO GROUP alext64
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018005353_39d090d2-26b7-46f7-9232-f4cea2f29514); Time taken: 0.204 seconds
INFO  : OK
No rows affected (0.475 seconds)
```

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20181018005454_b28132f2-00bb-488e-ba81-b6d1c990795d): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018005454_b28132f2-00bb-488e-ba81-b6d1c990795d); Time taken: 0.162 seconds
INFO  : Executing command(queryId=hive_20181018005454_b28132f2-00bb-488e-ba81-b6d1c990795d): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018005454_b28132f2-00bb-488e-ba81-b6d1c990795d); Time taken: 0.236 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.531 seconds)

```

### Create additional test users

```shell
sudo groupadd selector && sudo groupadd inserters && sudo useradd -u 1100 -g selector george && sudo useradd -u 1200 -g inserters ferdinand
kadmin  -p admin/admin

kadmin: add_principal george
kadmin: add_principal ferdinand
```

### Create test roles

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20181018011515_7a43bc31-4f5f-4cbb-8b1c-1c38d1adfcde): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018011515_7a43bc31-4f5f-4cbb-8b1c-1c38d1adfcde); Time taken: 0.175 seconds
INFO  : Executing command(queryId=hive_20181018011515_7a43bc31-4f5f-4cbb-8b1c-1c38d1adfcde): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018011515_7a43bc31-4f5f-4cbb-8b1c-1c38d1adfcde); Time taken: 0.052 seconds
INFO  : OK
No rows affected (0.365 seconds)

```

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20181018011515_a919f7ea-0072-4e78-b734-3ed1a225357a): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018011515_a919f7ea-0072-4e78-b734-3ed1a225357a); Time taken: 0.167 seconds
INFO  : Executing command(queryId=hive_20181018011515_a919f7ea-0072-4e78-b734-3ed1a225357a): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018011515_a919f7ea-0072-4e78-b734-3ed1a225357a); Time taken: 0.036 seconds
INFO  : OK
No rows affected (0.221 seconds)

```

### Grant read privilege for all tables to `reads`

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20181018012020_2b3efd2a-6c1b-437f-a303-e94a06e40f5e): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012020_2b3efd2a-6c1b-437f-a303-e94a06e40f5e); Time taken: 0.156 seconds
INFO  : Executing command(queryId=hive_20181018012020_2b3efd2a-6c1b-437f-a303-e94a06e40f5e): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012020_2b3efd2a-6c1b-437f-a303-e94a06e40f5e); Time taken: 0.091 seconds
INFO  : OK
No rows affected (0.264 seconds)

```

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20181018012020_c245057d-5244-4838-9a2b-530b5e37a04b): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012020_c245057d-5244-4838-9a2b-530b5e37a04b); Time taken: 0.163 seconds
INFO  : Executing command(queryId=hive_20181018012020_c245057d-5244-4838-9a2b-530b5e37a04b): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012020_c245057d-5244-4838-9a2b-530b5e37a04b); Time taken: 0.054 seconds
INFO  : OK
No rows affected (0.23 seconds)
```

### Grant read privilege for `default.sample07` only to 'writes':

```shell
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20181018012222_64f13a58-2c91-4cbc-be5d-697f8c4b999c): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012222_64f13a58-2c91-4cbc-be5d-697f8c4b999c); Time taken: 0.141 seconds
INFO  : Executing command(queryId=hive_20181018012222_64f13a58-2c91-4cbc-be5d-697f8c4b999c): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012222_64f13a58-2c91-4cbc-be5d-697f8c4b999c); Time taken: 0.095 seconds
INFO  : OK
No rows affected (0.252 seconds)
```

```
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20181018012222_1af2715b-f4fe-4278-ab98-9692f7e07246): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012222_1af2715b-f4fe-4278-ab98-9692f7e07246); Time taken: 0.154 seconds
INFO  : Executing command(queryId=hive_20181018012222_1af2715b-f4fe-4278-ab98-9692f7e07246): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012222_1af2715b-f4fe-4278-ab98-9692f7e07246); Time taken: 0.061 seconds
INFO  : OK
No rows affected (0.26 seconds)
```

```
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20181018012222_b807e635-2254-4c7d-b73c-34422748f383): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012222_b807e635-2254-4c7d-b73c-34422748f383); Time taken: 0.145 seconds
INFO  : Executing command(queryId=hive_20181018012222_b807e635-2254-4c7d-b73c-34422748f383): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012222_b807e635-2254-4c7d-b73c-34422748f383); Time taken: 0.042 seconds
INFO  : OK
No rows affected (0.198 seconds)
```

### `kinit` as george, then login to beeline

```shell
[alext@sebc02 ~]$ kinit george
Password for george@HADOOP.COM:
[alext@sebc02 ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.13.3 by Apache Hive
beeline> !connect jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.13.3)
Driver: Hive JDBC (version 1.1.0-cdh5.13.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20181018012424_d2d79e39-26f9-40ab-8445-a5be06a92fb2): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012424_d2d79e39-26f9-40ab-8445-a5be06a92fb2); Time taken: 0.168 seconds
INFO  : Executing command(queryId=hive_20181018012424_d2d79e39-26f9-40ab-8445-a5be06a92fb2): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012424_d2d79e39-26f9-40ab-8445-a5be06a92fb2); Time taken: 0.497 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.855 seconds)
```

### `kinit` as ferdinand, then login to beeline

```shell
[alext@sebc02 ~]$ kinit ferdinand
Password for ferdinand@HADOOP.COM:
[alext@sebc02 ~]$ beeline
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=512M; support was removed in 8.0
Beeline version 1.1.0-cdh5.13.3 by Apache Hive
beeline> !connect jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://sebc01.westeurope.cloudapp.azure.com:10000/default;principal=hive/sebc01.westeurope.cloudapp.azure.com@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.13.3)
Driver: Hive JDBC (version 1.1.0-cdh5.13.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://sebc01.westeurope.cloudapp.az> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20181018012929_a6d3051f-d53f-47a7-8522-9ad5f45e3a65): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20181018012929_a6d3051f-d53f-47a7-8522-9ad5f45e3a65); Time taken: 0.147 seconds
INFO  : Executing command(queryId=hive_20181018012929_a6d3051f-d53f-47a7-8522-9ad5f45e3a65): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20181018012929_a6d3051f-d53f-47a7-8522-9ad5f45e3a65); Time taken: 0.487 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.82 seconds)
```





