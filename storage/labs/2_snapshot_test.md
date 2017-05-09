Create a precious directory in HDFS; copy the ZIP course file into it.

	[root@ip-172-31-1-96 ~]# ll
	total 788
	-rwxrwxrwx 1 root root 276201 May  9 09:44 hadoop-mapreduce-examples.jar
	-rwxrwxrwx 1 root root  24341 May  8 13:53 mysql57-community-release-el5-8.noarch.rpm
	-rwxrwxrwx 1 root root  25664 May  8 12:29 mysql57-community-release-el6-11.noarch.rpm
	-rw-r--r-- 1 root root 474957 May  9 10:36 SEBC-Shanghai.zip
	[root@ip-172-31-1-96 ~]# hdfs dfs -mkdir /user/root/precious
	[root@ip-172-31-1-96 ~]# hdfs dfs -put SEBC-Shanghai.zip /user/root/precious


Enable snapshots for precious

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfsadmin -allowSnapshot /user/root/precious
	Allowing snaphot on /user/root/precious succeeded

Create a snapshot called sebc-hdfs-test

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -createSnapshot /user/root/precious sebc-hdfs-test
	Created snapshot /user/root/precious/.snapshot/sebc-hdfs-test


Delete the directory

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -rm -r /user/root/precious 
	rm: Failed to move to trash: hdfs://nameservice1/user/root/precious: The directory /user/root/precious cannot be deleted since /user/root/precious is snapshottable and already has snapshots

Delete the ZIP file

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -rm /user/root/precious/SEBC-Shanghai.zip
	17/05/09 10:56:54 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/root/precious/SEBC-Shanghai.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/root/precious/SEBC-Shanghai.zip

Restore the deleted file

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -ls /user/root/precious/
	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -cp /user/root/precious/.snapshot/sebc-hdfs-test/* /user/root/precious/
	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -ls /user/root/precious/                                                
	Found 1 items
	-rw-r--r--   3 hdfs root     474957 2017-05-09 11:05 /user/root/precious/SEBC-Shanghai.zip
