

*Configure the CM repo to install the latest release*

```shell
sudo vim /etc/yum.repos.d/cloudera-manager.repo

[cloudera-manager]
name = Cloudera Manager, Version 5.14.4
baseurl = http://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5.14.4
gpgkey = http://archive.cloudera.com/redhat/cdh/RPM-GPG-KEY-cloudera
gpgcheck = 1
```

*List the server repo files*

```shell
[alext@sebx02 ~]$ ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-Media.repo      mysql-community.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo      mysql-community-source.repo
CentOS-fasttrack.repo  cloudera-manager.repo  OpenLogic.repo

```

*Install CM*

```shell
Dependencies Resolved

================================================================================
 Package                 Arch   Version                  Repository        Size
================================================================================
Installing:
 cloudera-manager-server x86_64 5.14.4-1.cm5144.p0.3.el6 cloudera-manager 8.5 k
Installing for dependencies:
 cloudera-manager-daemons
                         x86_64 5.14.4-1.cm5144.p0.3.el6 cloudera-manager 765 M

Transaction Summary
================================================================================
Install       2 Package(s)
```

*Ensuring the start at boot time*

```shell
sudo chkconfig cloudera-scm-server on
```

*Preparing CM Database*

```shell
[alext@sebx02 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh  mysql  -h sebx01.westeurope.cloudapp.azure.com scm scm Amon_amon1   

JAVA_HOME=/usr/java/default
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/default/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
Fri Oct 19 08:34:18 UTC 2018 WARN: Establishing SSL connection without server's identity verification is not recommended. According to MySQL 5.5.45+, 5.6.26+ and 5.7.6+ requirements SSL connection must be established by default if explicit option isn't set. For compliance with existing applications not using SSL the verifyServerCertificate property is set to 'false'. You need either to explicitly disable SSL by setting useSSL=false, or set useSSL=true and provide truststore for server certificate verification.
2018-10-19 08:34:19,417 [main] INFO  com.cloudera.enterprise.dbutil.DbCommandExecutor  - Successfully connected to database.
All done, your SCM database is configured correctly!

```

