- List the cloud provider you are using (AWS, GCE, Azure, other)

  AWS

- List the Linux release you have chosen

  ```shell
  cat /etc/redhat-release
  CentOS release 6.10 (Final)
  ```

- Show that the disk space on each node is at least 30 GB

  ```shell
  [alext@sebx01 ~]$ df -h
  Filesystem      Size  Used Avail Use% Mounted on
  /dev/sda1        30G  2.6G   26G  10% /
  tmpfs           7.9G     0  7.9G   0% /dev/shm
  /dev/sdb1        79G   56M   75G   1% /mnt/resource
  /dev/sdc5        50G   52M   49G   1% /data/1
  /dev/sdc6        50G   52M   49G   1% /data/2
  /dev/sdc7        50G   52M   49G   1% /data/3
  /dev/sdc8        50G   52M   49G   1% /data/4
  /dev/sdc9        50G   52M   49G   1% /data/5
  ```



```shell
[alext@sebx02 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        30G  2.5G   26G   9% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
/dev/sdb1        79G   56M   75G   1% /mnt/resource
/dev/sdc5        50G   52M   49G   1% /data/1
/dev/sdc6        50G   52M   49G   1% /data/2
/dev/sdc7        50G   52M   49G   1% /data/3
/dev/sdc8        50G   52M   49G   1% /data/4
/dev/sdc9        50G   52M   49G   1% /data/5

```



```shell
[alext@sebx03 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        30G  2.6G   26G   9% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
/dev/sdb1        79G   56M   75G   1% /mnt/resource
/dev/sdc5        50G   52M   49G   1% /data/1
/dev/sdc6        50G   52M   49G   1% /data/2
/dev/sdc7        50G   52M   49G   1% /data/3
/dev/sdc8        50G   52M   49G   1% /data/4
/dev/sdc9        50G   52M   49G   1% /data/5

```



```shell
[alext@sebx04 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        30G  2.5G   26G   9% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
/dev/sdb1        79G   56M   75G   1% /mnt/resource
/dev/sdc5        50G   52M   49G   1% /data/1
/dev/sdc6        50G   52M   49G   1% /data/2
/dev/sdc7        50G   52M   49G   1% /data/3
/dev/sdc8        50G   52M   49G   1% /data/4
/dev/sdc9        50G   52M   49G   1% /data/5

```



```shell
[alext@sebx05 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        30G  2.6G   26G   9% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
/dev/sdb1        79G   56M   75G   1% /mnt/resource
/dev/sdc5        50G   52M   49G   1% /data/1
/dev/sdc6        50G   52M   49G   1% /data/2
/dev/sdc7        50G   52M   49G   1% /data/3
/dev/sdc8        50G   52M   49G   1% /data/4
/dev/sdc9        50G   52M   49G   1% /data/5

```



- List the command and output for `yum repolist enabled`

```shell
[alext@sebx01 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, security
Determining fastest mirrors
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql80-community                                        | 2.5 kB     00:00
openlogic                                                | 2.9 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                       repo name                                   status
base                          CentOS-6 - Base                             6,713
extras                        CentOS-6 - Extras                              33
mysql-connectors-community    MySQL Connectors Community                     59
mysql-tools-community         MySQL Tools Community                          65
mysql80-community             MySQL 8.0 Community Server                     29
openlogic                     CentOS-6 - openlogic packages for x86_64      104
updates                       CentOS-6 - Updates                            205
repolist: 7,208
```



```shell
[alext@sebx02 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, security
Determining fastest mirrors
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-connectors-community/primary_db                    |  24 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql-tools-community/primary_db                         |  43 kB     00:00
mysql80-community                                        | 2.5 kB     00:00
mysql80-community/primary_db                             |  27 kB     00:00
openlogic                                                | 2.9 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                       repo name                                   status
base                          CentOS-6 - Base                             6,713
extras                        CentOS-6 - Extras                              33
mysql-connectors-community    MySQL Connectors Community                     59
mysql-tools-community         MySQL Tools Community                          65
mysql80-community             MySQL 8.0 Community Server                     29
openlogic                     CentOS-6 - openlogic packages for x86_64      104
updates                       CentOS-6 - Updates                            205
repolist: 7,208

```



```shell
[alext@sebx03 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, security
Determining fastest mirrors
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-connectors-community/primary_db                    |  24 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql-tools-community/primary_db                         |  43 kB     00:00
mysql80-community                                        | 2.5 kB     00:00
mysql80-community/primary_db                             |  27 kB     00:00
openlogic                                                | 2.9 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                       repo name                                   status
base                          CentOS-6 - Base                             6,713
extras                        CentOS-6 - Extras                              33
mysql-connectors-community    MySQL Connectors Community                     59
mysql-tools-community         MySQL Tools Community                          65
mysql80-community             MySQL 8.0 Community Server                     29
openlogic                     CentOS-6 - openlogic packages for x86_64      104
updates                       CentOS-6 - Updates                            205
repolist: 7,208

```



```shell
[alext@sebx04 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, security
Determining fastest mirrors
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-connectors-community/primary_db                    |  24 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql-tools-community/primary_db                         |  43 kB     00:00
mysql80-community                                        | 2.5 kB     00:00
mysql80-community/primary_db                             |  27 kB     00:00
openlogic                                                | 2.9 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                       repo name                                   status
base                          CentOS-6 - Base                             6,713
extras                        CentOS-6 - Extras                              33
mysql-connectors-community    MySQL Connectors Community                     59
mysql-tools-community         MySQL Tools Community                          65
mysql80-community             MySQL 8.0 Community Server                     29
openlogic                     CentOS-6 - openlogic packages for x86_64      104
updates                       CentOS-6 - Updates                            205
repolist: 7,208

```



```shell
[alext@sebx05 ~]$ yum repolist enabled
Loaded plugins: fastestmirror, security
Determining fastest mirrors
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-connectors-community/primary_db                    |  24 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql-tools-community/primary_db                         |  43 kB     00:00
mysql80-community                                        | 2.5 kB     00:00
mysql80-community/primary_db                             |  27 kB     00:00
openlogic                                                | 2.9 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                       repo name                                   status
base                          CentOS-6 - Base                             6,713
extras                        CentOS-6 - Extras                              33
mysql-connectors-community    MySQL Connectors Community                     59
mysql-tools-community         MySQL Tools Community                          65
mysql80-community             MySQL 8.0 Community Server                     29
openlogic                     CentOS-6 - openlogic packages for x86_64      104
updates                       CentOS-6 - Updates                            205
repolist: 7,208

```



- Add the following Linux accounts to all nodes

  - User `raffles` with a UID of `2000`

    ```shell
    sudo useradd -u 2000 raffles
    ```

  - User `fullerton` with a UID of `3000`

    ```shell
    sudo useradd -u 3000 fullerton
    ```

  - Create the group `hotels` and add `fullerton` to it

    ```shell
    sudo groupadd hotels
    sudo usermod -aG hotels fullerton
    ```

  - Create the group `shops` and add `raffles` to it

    ```shell
    sudo groupadd shops
    sudo usermod -aG shops raffles
    ```

- List the `/etc/passwd` entries for `raffles` and `fullerton` in your setup file

  ```shell
  [alext@sebx01 ~]$ grep raffles /etc/passwd
  raffles:x:2000:2000::/home/raffles:/bin/bash
  
  [alext@sebx01 ~]$ grep fullerton /etc/passwd
  fullerton:x:3000:3000::/home/fullerton:/bin/bash
  ```

- List the `/etc/group` entries for `hotels` and `shops` in your setup file

  ```shell
  [alext@sebx01 ~]$ grep hotels /etc/group
  hotels:x:3001:fullerton
  
  [alext@sebx01 ~]$ grep shops /etc/group
  shops:x:3002:raffles
  ```
