Install a compatible MySQL or MariaDB server on the node you listed first

*Install the repo file*

```shell
[alext@sebx01 ~]$ sudo sudo yum install mysql80-community-release-el6-1.noarch.rpm
```

*Enable mysql 5.7 version and disable the 8.0 (enabled by default) on all nodes*

```shell
sudo vim /etc/yum.repos.d/mysql-community.repo
# Enable to use MySQL 5.7
[mysql57-community]
name=MySQL 5.7 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.7-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql80-community]
name=MySQL 8.0 Community Server
baseurl=http://repo.mysql.com/yum/mysql-8.0-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
...
sudo yum update
```

```shell
[alext@sebx01 ~]$ sudo yum update

Dependencies Resolved

================================================================================
 Package                      Arch    Version          Repository          Size
================================================================================
Installing:
 mysql-community-libs         x86_64  5.7.23-1.el6     mysql57-community  2.1 M
     replacing  mysql-libs.x86_64 5.1.73-8.el6_8
 mysql-community-libs-compat  x86_64  5.7.23-1.el6     mysql57-community  1.6 M
     replacing  mysql-libs.x86_64 5.1.73-8.el6_8
Installing for dependencies:
 mysql-community-common       x86_64  5.7.23-1.el6     mysql57-community  332 k

Transaction Summary
================================================================================
Install       3 Package(s)
```

```shell
[alext@sebx01 ~]$ sudo yum install mysql-community-server
Dependencies Resolved

================================================================================
 Package                   Arch      Version         Repository            Size
================================================================================
Installing:
 mysql-community-server    x86_64    5.7.23-1.el6    mysql57-community    153 M
Installing for dependencies:
 mysql-community-client    x86_64    5.7.23-1.el6    mysql57-community     23 M

Transaction Summary
================================================================================
Install       2 Package(s)
```

```shell
sudo chkconfig mysqld on
sudo service mysqld start
sudo /usr/bin/mysql_secure_installation
```

- On all cluster nodes

  - Install the MySQL client package and JDBC connector jar

    ```shell
    sudo yum install mysql-community-client -y
    
    [alext@sebx02 ~]$ sudo yum list mysql-community-client
    Loaded plugins: fastestmirror, security
    Loading mirror speeds from cached hostfile
    Installed Packages
    mysql-community-client.x86_64          5.7.23-1.el6           @mysql57-community
    ```

    ```shell
    sudo wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.46.tar.gz
    sudo tar zxvf mysql-connector-java-5.1.46.tar.gz
    sudo mkdir -p /usr/share/java/ 
    cd mysql-connector-java-5.1.46 
    sudo cp mysql-connector-java-5.1.46-bin.jar /usr/share/java/mysql-connector-java.jar
    
    [alext@sebx02 ~]$ ls -la /usr/share/java/mysql-connector-java.jar
    -rw-r--r--. 1 root root 1004840 Oct 18 14:12 /usr/share/java/mysql-connector-java.jar
    ```

- Create the following databases

  - `scm`

  - `rman`

  - `hive`

  - `oozie`

  - `hue`

  - `sentry`

    ```shell
    CREATE DATABASE scm DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    CREATE DATABASE rman DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    CREATE DATABASE hue DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    CREATE DATABASE hive DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    CREATE DATABASE sentry DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    CREATE DATABASE oozie DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
    
    GRANT ALL ON scm.* TO 'scm'@'%' IDENTIFIED BY 'Amon_amon1';
    GRANT ALL ON rman.* TO 'rman'@'%' IDENTIFIED BY 'Amon_amon1';
    GRANT ALL ON hue.* TO 'hue'@'%' IDENTIFIED BY 'Amon_amon1';
    GRANT ALL ON hive.* TO 'hive'@'%' IDENTIFIED BY 'Amon_amon1';
    GRANT ALL ON sentry.* TO 'sentry'@'%' IDENTIFIED BY 'Amon_amon1';
    GRANT ALL ON oozie.* TO 'oozie'@'%' IDENTIFIED BY 'Amon_amon1';
    ```


- The hostname of your DB node

  ```shell
  mysql> SHOW VARIABLES like 'hostname';
  +---------------+--------------------------------------+
  | Variable_name | Value                                |
  +---------------+--------------------------------------+
  | hostname      | sebx01.westeurope.cloudapp.azure.com |
  +---------------+--------------------------------------+
  ```

- The command screenshot to display the DB version

  ```
  mysql> select version();
  +-----------+
  | version() |
  +-----------+
  | 5.7.23    |
  +-----------+
  ```

- The command and output for listing databases

  ```
  mysql> show databases;
  +--------------------+
  | Database           |
  +--------------------+
  | information_schema |
  | hive               |
  | hue                |
  | mysql              |
  | oozie              |
  | performance_schema |
  | rman               |
  | scm                |
  | sentry             |
  | sys                |
  +--------------------+
  
  ```
