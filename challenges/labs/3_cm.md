- Create user directories in HDFS for `raffles` and `fullerton`

  ```shell
  sudo -E su - hdfs -c "hadoop fs -mkdir /user/raffles/"
  sudo -E su - hdfs -c "hadoop fs -chown raffles:raffles /user/raffles/"
  
  sudo -E su - hdfs -c "hadoop fs -mkdir /user/fullerton/"
  sudo -E su - hdfs -c "hadoop fs -chown fullerton:fullerton /user/fullerton/"
  ```

  *and list /user*

  ```shell
  [alext@sebx01 ~]$ hdfs dfs -ls /user
  Found 6 items
  drwxr-xr-x   - fullerton fullerton          0 2018-10-19 09:19 /user/fullerton
  drwxrwxrwx   - mapred    hadoop             0 2018-10-19 09:17 /user/history
  drwxrwxr-t   - hive      hive               0 2018-10-19 09:19 /user/hive
  drwxrwxr-x   - hue       hue                0 2018-10-19 09:19 /user/hue
  drwxrwxr-x   - oozie     oozie              0 2018-10-19 09:20 /user/oozie
  drwxr-xr-x   - raffles   raffles            0 2018-10-19 09:19 /user/raffles
  ```

  *List the output of this api call*	

```
http://sebx02.westeurope.cloudapp.azure.com:7180/api/v14/hosts
```

```json
{
  "items" : [ {
    "hostId" : "a5b8c9d9-b22e-4754-9006-9bc2af02054d",
    "ipAddress" : "10.0.0.4",
    "hostname" : "sebx01.westeurope.cloudapp.azure.com",
    "rackId" : "/default",
    "hostUrl" : "http://sebx02.westeurope.cloudapp.azure.com:7180/cmf/hostRedirect/a5b8c9d9-b22e-4754-9006-9bc2af02054d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 8,
    "totalPhysMemBytes" : 16845422592
  }, {
    "hostId" : "8bf8546f-2a06-4327-95cc-3f6671870ffe",
    "ipAddress" : "10.0.0.5",
    "hostname" : "sebx02.westeurope.cloudapp.azure.com",
    "rackId" : "/default",
    "hostUrl" : "http://sebx02.westeurope.cloudapp.azure.com:7180/cmf/hostRedirect/8bf8546f-2a06-4327-95cc-3f6671870ffe",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 8,
    "totalPhysMemBytes" : 16845422592
  }, {
    "hostId" : "fba8f128-71a0-4e3d-81df-ae20761b50ab",
    "ipAddress" : "10.0.0.6",
    "hostname" : "sebx03.westeurope.cloudapp.azure.com",
    "rackId" : "/default",
    "hostUrl" : "http://sebx02.westeurope.cloudapp.azure.com:7180/cmf/hostRedirect/fba8f128-71a0-4e3d-81df-ae20761b50ab",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 8,
    "totalPhysMemBytes" : 16845422592
  }, {
    "hostId" : "d1c52cd5-fe24-46f4-a5c0-24ea3fa0c0b5",
    "ipAddress" : "10.0.0.7",
    "hostname" : "sebx04.westeurope.cloudapp.azure.com",
    "rackId" : "/default",
    "hostUrl" : "http://sebx02.westeurope.cloudapp.azure.com:7180/cmf/hostRedirect/d1c52cd5-fe24-46f4-a5c0-24ea3fa0c0b5",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 8,
    "totalPhysMemBytes" : 16845422592
  }, {
    "hostId" : "be892bf7-d0a0-467a-acbe-13b7d22370f7",
    "ipAddress" : "10.0.0.8",
    "hostname" : "sebx05.westeurope.cloudapp.azure.com",
    "rackId" : "/default",
    "hostUrl" : "http://sebx02.westeurope.cloudapp.azure.com:7180/cmf/hostRedirect/be892bf7-d0a0-467a-acbe-13b7d22370f7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 8,
    "totalPhysMemBytes" : 16845422592
  } ]
}
```

