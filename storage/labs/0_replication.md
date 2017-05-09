Use teragen to create a 500 MB file

	[root@ip-172-31-1-96 ~]# hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapred.map.tasks=3 5242880 /user/root/wk109353794
	17/05/09 08:09:20 INFO terasort.TeraSort: Generating 5242880 using 3
	17/05/09 08:09:20 INFO mapreduce.JobSubmitter: number of splits:3
	17/05/09 08:09:20 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
	17/05/09 08:09:21 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494310619863_0001
	17/05/09 08:09:21 INFO impl.YarnClientImpl: Submitted application application_1494310619863_0001
	17/05/09 08:09:21 INFO mapreduce.Job: The url to track the job: http://ip-172-31-1-96.us-west-1.compute.internal:8088/proxy/application_1494310619863_0001/
	17/05/09 08:09:21 INFO mapreduce.Job: Running job: job_1494310619863_0001
	17/05/09 08:09:29 INFO mapreduce.Job: Job job_1494310619863_0001 running in uber mode : false
	17/05/09 08:09:29 INFO mapreduce.Job:  map 0% reduce 0%
	17/05/09 08:09:39 INFO mapreduce.Job:  map 33% reduce 0%
	17/05/09 08:09:42 INFO mapreduce.Job:  map 100% reduce 0%
	17/05/09 08:09:43 INFO mapreduce.Job: Job job_1494310619863_0001 completed successfully
	17/05/09 08:09:43 INFO mapreduce.Job: Counters: 31
			File System Counters
					FILE: Number of bytes read=0
					FILE: Number of bytes written=385530
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=252
					HDFS: Number of bytes written=524288000
					HDFS: Number of read operations=12
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=6
			Job Counters 
					Launched map tasks=3
					Other local map tasks=3
					Total time spent by all maps in occupied slots (ms)=28144
					Total time spent by all reduces in occupied slots (ms)=0
					Total time spent by all map tasks (ms)=28144
					Total vcore-seconds taken by all map tasks=28144
					Total megabyte-seconds taken by all map tasks=28819456
			Map-Reduce Framework
					Map input records=5242880
					Map output records=5242880
					Input split bytes=252
					Spilled Records=0
					Failed Shuffles=0
					Merged Map outputs=0
					GC time elapsed (ms)=309
					CPU time spent (ms)=17600
					Physical memory (bytes) snapshot=1081585664
					Virtual memory (bytes) snapshot=4703318016
					Total committed heap usage (bytes)=1269301248
			org.apache.hadoop.examples.terasort.TeraGen$Counters
					CHECKSUM=11257830824958050
			File Input Format Counters 
					Bytes Read=0
			File Output Format Counters 
					Bytes Written=524288000



Use hdfs fsck <path> -files -blocks on your source and target directories

	[hdfs@ip-172-31-1-96 ~]$ hdfs fsck /user/root/ -files -blocks      
	Connecting to namenode via http://ip-172-31-1-96.us-west-1.compute.internal:50070
	FSCK started by hdfs (auth:SIMPLE) from /172.31.1.96 for path /user/root/ at Tue May 09 09:34:42 UTC 2017
	/user/root/ <dir>
	/user/root/.staging <dir>
	/user/root/wk109353794 <dir>
	/user/root/wk109353794/_SUCCESS 0 bytes, 0 block(s):  OK
	
	/user/root/wk109353794/part-m-00000 174762700 bytes, 2 block(s):  OK
	0. BP-761789631-172.31.1.96-1494307860548:blk_1073742657_1833 len=134217728 Live_repl=3
	1. BP-761789631-172.31.1.96-1494307860548:blk_1073742660_1836 len=40544972 Live_repl=3
	
	/user/root/wk109353794/part-m-00001 174762700 bytes, 2 block(s):  OK
	0. BP-761789631-172.31.1.96-1494307860548:blk_1073742658_1834 len=134217728 Live_repl=3
	1. BP-761789631-172.31.1.96-1494307860548:blk_1073742663_1839 len=40544972 Live_repl=3
	
	/user/root/wk109353794/part-m-00002 174762600 bytes, 2 block(s):  OK
	0. BP-761789631-172.31.1.96-1494307860548:blk_1073742659_1835 len=134217728 Live_repl=3
	1. BP-761789631-172.31.1.96-1494307860548:blk_1073742662_1838 len=40544872 Live_repl=3
	
	Status: HEALTHY
	Total size:    524288000 B
	Total dirs:    3
	Total files:   4
	Total symlinks:                0
	Total blocks (validated):      6 (avg. block size 87381333 B)
	Minimally replicated blocks:   6 (100.0 %)
	Over-replicated blocks:        0 (0.0 %)
	Under-replicated blocks:       0 (0.0 %)
	Mis-replicated blocks:         0 (0.0 %)
	Default replication factor:    3
	Average block replication:     3.0
	Corrupt blocks:                0
	Missing replicas:              0 (0.0 %)
	Number of data-nodes:          3
	Number of racks:               1
	FSCK ended at Tue May 09 09:34:42 UTC 2017 in 4 milliseconds
	
	
	The filesystem under path '/user/root/' is HEALTHY