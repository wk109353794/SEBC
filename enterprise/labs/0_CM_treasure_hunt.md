What is ubertask optimization?

- It is an option in YARN 
- Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

Where in CM is the Kerberos Security Realm value displayed?

- Kerberos Security Realm value displays in 'Admimistration -> Settings'

Which CDH service(s) host a property for enabling Kerberos authentication?

- Zookeeper

How do you upgrade the CM agents?

- Hosts -> All Hosts -> Re-run Upgrade Wizard

Give the tsquery statement used to chart Hue's CPU utilization?

- SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-HUE_SERVER-b3f39c9653941ed458a323dc32878b29" AND category = ROLE

Name all the roles that make up the Hive service

- Hive Metastore Server
- WebHCat Server
- HiveServer2 
- Gateway
 

What steps must be completed before integrating Cloudera Manager with Kerberos?

- Install Kerberos server and client
- Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC