**Api version**

```shell
curl -u alext64:cloudera 'http://localhost:7180/api/version'
```

```json
v19
```

**CM version**

```
curl -u alext64:cloudera 'http://localhost:7180/api/v19/cm/version'
```

```json
{
  "version" : "5.14.4",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20180707-0439",
  "gitHash" : "0971e84bdceb60db9b96533f46451f40ed8cbdf9",
  "snapshot" : false
}
```

**CM users**

```shell
curl -u alext64:cloudera 'http://localhost:7180/api/v19/users'
```

```json
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "alext64",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

**CM db**

```shell
curl -u alext64:cloudera 'http://localhost:7180/api/v19/cm/scmDbInfo'
```

```json
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```

