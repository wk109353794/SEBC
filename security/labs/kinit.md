	[root@ip-172-31-1-58 ~]# kinit -k -t wk109353794.keytab wk109353794@WKSEBC.COM   
	[root@ip-172-31-1-58 ~]# klist
	Ticket cache: FILE:/tmp/krb5cc_0
	Default principal: wk109353794@WKSEBC.COM
	
	Valid starting     Expires            Service principal
	05/11/17 03:38:43  05/12/17 03:38:43  krbtgt/WKSEBC.COM@WKSEBC.COM
			renew until 05/18/17 03:38:43
	[root@ip-172-31-1-58 ~]# hdfs dfs -ls /user/
	Found 4 items
	drwxrwxrwx   - mapred hadoop          0 2017-05-10 10:49 /user/history
	drwxrwxr-t   - hive   hive            0 2017-05-10 10:54 /user/hive
	drwxrwxr-x   - hue    hue             0 2017-05-10 10:55 /user/hue
	drwxrwxr-x   - oozie  oozie           0 2017-05-10 11:00 /user/oozie