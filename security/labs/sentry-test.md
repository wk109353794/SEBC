
	beeline>!connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	1: jdbc:hive2://localhost:10000/default> SHOW TABLES;
	INFO  : Compiling command(queryId=hive_20170511053030_7ec789f5-3057-4f9f-ae3d-2ef512a10445): SHOW TABLES
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170511053030_7ec789f5-3057-4f9f-ae3d-2ef512a10445); Time taken: 0.085 seconds
	INFO  : Executing command(queryId=hive_20170511053030_7ec789f5-3057-4f9f-ae3d-2ef512a10445): SHOW TABLES
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170511053030_7ec789f5-3057-4f9f-ae3d-2ef512a10445); Time taken: 0.155 seconds
	INFO  : OK
	+-----------+--+
	| tab_name  |
	+-----------+--+
	+-----------+--+
	No rows selected (0.362 seconds)
	1: jdbc:hive2://localhost:10000/default> 

After create a Sentry role with full authorization

	0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
	INFO  : Compiling command(queryId=hive_20170511063737_90ec4edc-8275-481e-af35-02b083cc6049): SHOW TABLES
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170511063737_90ec4edc-8275-481e-af35-02b083cc6049); Time taken: 0.095 seconds
	INFO  : Executing command(queryId=hive_20170511063737_90ec4edc-8275-481e-af35-02b083cc6049): SHOW TABLES
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170511063737_90ec4edc-8275-481e-af35-02b083cc6049); Time taken: 0.157 seconds
	INFO  : OK
	+------------+--+
	|  tab_name  |
	+------------+--+
	| importlog  |
	+------------+--+
	1 row selected (0.395 seconds)
	0: jdbc:hive2://localhost:10000/default> 

kinit as george,ferdinand

	[root@ip-172-31-1-58 ~]# kinit george@WKSEBC.COM
	Password for george@WKSEBC.COM: 
	[root@ip-172-31-1-58 ~]# klist  
	Ticket cache: FILE:/tmp/krb5cc_0
	Default principal: george@WKSEBC.COM
	
	Valid starting     Expires            Service principal
	05/11/17 07:54:59  05/12/17 07:54:59  krbtgt/WKSEBC.COM@WKSEBC.COM
			renew until 05/18/17 07:54:59
	[root@ip-172-31-1-58 ~]# beeline
	Beeline version 1.1.0-cdh5.9.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20170511075555_ded9f8b9-78b1-4c5e-9e89-de51bf5ae4c5): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170511075555_ded9f8b9-78b1-4c5e-9e89-de51bf5ae4c5); Time taken: 0.071 seconds
	INFO  : Executing command(queryId=hive_20170511075555_ded9f8b9-78b1-4c5e-9e89-de51bf5ae4c5): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170511075555_ded9f8b9-78b1-4c5e-9e89-de51bf5ae4c5); Time taken: 0.13 seconds
	INFO  : OK
	+-----------+--+
	| tab_name  |
	+-----------+--+
	| importlog  |
	| sample07   |
	+-----------+--+
	No rows selected (0.296 seconds)
	0: jdbc:hive2://localhost:10000/default> !q
	Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	[root@ip-172-31-1-58 ~]# kinit ferdinand@WKSEBC.COM
	Password for ferdinand@WKSEBC.COM: 
	[root@ip-172-31-1-58 ~]# klist
	Ticket cache: FILE:/tmp/krb5cc_0
	Default principal: ferdinand@WKSEBC.COM
	
	Valid starting     Expires            Service principal
	05/11/17 07:56:38  05/12/17 07:56:38  krbtgt/WKSEBC.COM@WKSEBC.COM
			renew until 05/18/17 07:56:38
	[root@ip-172-31-1-58 ~]# beeline
	Beeline version 1.1.0-cdh5.9.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-1-58.us-west-1.compute.internal@WKSEBC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20170511075757_3724bea2-6a3e-4bed-ad6c-2b007852d406): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20170511075757_3724bea2-6a3e-4bed-ad6c-2b007852d406); Time taken: 0.076 seconds
	INFO  : Executing command(queryId=hive_20170511075757_3724bea2-6a3e-4bed-ad6c-2b007852d406): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20170511075757_3724bea2-6a3e-4bed-ad6c-2b007852d406); Time taken: 0.155 seconds
	INFO  : OK
	+-----------+--+
	| tab_name  |
	+-----------+--+
	| sample07   |
	+-----------+--+
	No rows selected (0.33 seconds)