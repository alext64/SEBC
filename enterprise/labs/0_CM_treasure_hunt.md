1. What is ubertask optimization?

   *Ubertask optimization is enabled to run "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.*

2. Where in CM is the Kerberos Security Realm value displayed?

   *You can set it in "Kerberos Security Realm" setting or just see the default: "HADOOP.COM".* 

3. Which CDH service(s) host a property for enabling Kerberos authentication?

   *In a CDH Coreset Installed Cluster (our bootcamp cluster) just Zookeeper, HDFS and YARN.*

4. How do you upgrade the CM agents?

   *You can upgrade CM agents via the CM wizard, during an upgrade assessment, or manually upgrading the agent installation in every cluster server via OS bounded script.*

5. Give the `tsquery` statement used to chart Hue's CPU utilization?

   *select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName="hue"*.

6. Name all the roles that make up the Hive service

   *Gateway, Hive Metastore Server, HiveServer2, WebHCatServer.*

7. What steps must be completed before integrating Cloudera Manager with Kerberos?

   **.** Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.

   **.** The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. CDH will not work properly if tickets are not renewable.

   **.** OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.

   **.** Cloudera Manager needs an account that has permissions to create other accounts in the KDC.

