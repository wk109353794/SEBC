
The hostname of your database server

	ip-172-31-1-194.us-west-1.compute.internal	172.31.1.194

The command and output for showing the database server version
	
	[root@ip-172-31-1-194 ~]# mysql -V
	mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper

The command and output for listing the databases created above
	
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
	+--------------------+
	9 rows in set (0.00 sec)
