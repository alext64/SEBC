**Stopping Hive service**

```shell
curl -X POST -u alext64:cloudera 'http://localhost:7180/api/v12/clusters/alext64/services/hive/commands/stop'
```



```json
{
  "id" : 739,
  "name" : "Stop",
  "startTime" : "2018-10-17T09:22:18.978Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

**Starting Hive service**

```shell
curl -X POST -u alext64:cloudera 'http://localhost:7180/api/v12/clusters/alext64/services/hive/commands/start'
```



```json
{
  "id" : 743,
  "name" : "Start",
  "startTime" : "2018-10-17T09:23:30.933Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

**Querying about Hive service status**

```shell
curl -u alext64:cloudera 'http://localhost:7180/api/v12/clusters/alext64/services/hive/'
```



```json
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://10.0.0.9:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://10.0.0.9:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"

```

