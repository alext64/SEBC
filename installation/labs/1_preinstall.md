**Cloudera 5.13.3 Installation**

Created 5 Vm-scalegrid.centos-free-20181015135542, 

8 cpu 16 GB ram, 

Centos 6.8 --> 6.10 with yum upgrade

with a 30 GB root partition (+80 GB free) 

and a second volume of 256 GB for data directories.

Created 5 data directories in /data.

sudo yum install net-tools telnet openssl-perl vim ntp nscd

sudo chkconfig ip6tables off
sudo chkconfig iptables off
sudo chkconfig ntpd on
sudo chkconfig nscd on

vim /etc/selinux/config --> SELINUX=disabled

1. sudo bash -c "echo 'vm.swappiness = 1' >> /etc/sysctl.conf" && sudo sysctl vm.swappiness=1

![1539619475894](./1539619475894.png)



echo $HOSTNAME

![1539642083172](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539642083172.png)

sudo mkdir -p /data/1 /data/2 /data/3 /data/4 /data/5

sudo fdisk /dev/sdc --> create one extended partition (256 GB) e 5 logical subpartition (50GB)

sudo mkfs -t ext4 /dev/sdc5 && sudo tune2fs -m 1 /dev/sdc5
sudo mkfs -t ext4 /dev/sdc6 && sudo tune2fs -m 1 /dev/sdc6
sudo mkfs -t ext4 /dev/sdc7 && sudo tune2fs -m 1 /dev/sdc7
sudo mkfs -t ext4 /dev/sdc8 && sudo tune2fs -m 1 /dev/sdc8
sudo mkfs -t ext4 /dev/sdc9 && sudo tune2fs -m 1 /dev/sdc9
mount -a

2. mount -v
![1539642211527](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539642211527.png)

3. 

![1539619386138](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539619386138.png)

4. sudo bash -c "echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag"

   sudo less "/sys/kernel/mm/transparent_hugepage/defrag" 

   ![1539619561732](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539619561732.png)

   sudo vim /etc/rc.local

   ![1539642019868](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539642019868.png)

5. ![1539623204125](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539623204125.png)

6.

![1539618689781](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539618689781.png)

![1539642483032](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539642483032.png)

7.

![1539618746017](C:\Users\w8\AppData\Roaming\Typora\typora-user-images\1539618746017.png)

