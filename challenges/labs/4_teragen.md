The full teragen command and job output

	[zhou@ip-172-31-1-194 ~]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen \
	> -Dmapred.map.tasks=4 \
	> -Ddfs.block.size=64 \
	> -Dmapreduce.map.memory.mb=1024 \
	>  65536000 /user/zhou/tgen
	17/05/12 03:56:15 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-1-194.us-west-1.compute.internal/172.31.1.194:8032
	17/05/12 03:56:15 INFO terasort.TeraSort: Generating 65536000 using 4
	17/05/12 03:56:15 INFO mapreduce.JobSubmitter: number of splits:4
	17/05/12 03:56:16 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
	17/05/12 03:56:16 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494561292750_0002
	17/05/12 03:56:16 INFO impl.YarnClientImpl: Submitted application application_1494561292750_0002
	17/05/12 03:56:16 INFO mapreduce.Job: The url to track the job: http://ip-172-31-1-194.us-west-1.compute.internal:8088/proxy/application_1494561292750_0002/
	17/05/12 03:56:16 INFO mapreduce.Job: Running job: job_1494561292750_0002
	17/05/12 03:56:25 INFO mapreduce.Job: Job job_1494561292750_0002 running in uber mode : false
	17/05/12 03:56:25 INFO mapreduce.Job:  map 0% reduce 0%
	17/05/12 03:56:39 INFO mapreduce.Job:  map 13% reduce 0%
	17/05/12 03:56:42 INFO mapreduce.Job:  map 22% reduce 0%
	17/05/12 03:56:45 INFO mapreduce.Job:  map 27% reduce 0%
	17/05/12 03:56:48 INFO mapreduce.Job:  map 30% reduce 0%
	17/05/12 03:56:51 INFO mapreduce.Job:  map 34% reduce 0%
	17/05/12 03:56:54 INFO mapreduce.Job:  map 38% reduce 0%
	17/05/12 03:56:57 INFO mapreduce.Job:  map 42% reduce 0%
	17/05/12 03:57:00 INFO mapreduce.Job:  map 45% reduce 0%
	17/05/12 03:57:03 INFO mapreduce.Job:  map 49% reduce 0%
	17/05/12 03:57:06 INFO mapreduce.Job:  map 54% reduce 0%
	17/05/12 03:57:09 INFO mapreduce.Job:  map 57% reduce 0%
	17/05/12 03:57:12 INFO mapreduce.Job:  map 61% reduce 0%
	17/05/12 03:57:15 INFO mapreduce.Job:  map 65% reduce 0%
	17/05/12 03:57:18 INFO mapreduce.Job:  map 69% reduce 0%
	17/05/12 03:57:21 INFO mapreduce.Job:  map 74% reduce 0%
	17/05/12 03:57:24 INFO mapreduce.Job:  map 77% reduce 0%
	17/05/12 03:57:27 INFO mapreduce.Job:  map 81% reduce 0%
	17/05/12 03:57:30 INFO mapreduce.Job:  map 85% reduce 0%
	17/05/12 03:57:33 INFO mapreduce.Job:  map 89% reduce 0%
	17/05/12 03:57:36 INFO mapreduce.Job:  map 92% reduce 0%
	17/05/12 03:57:38 INFO mapreduce.Job:  map 93% reduce 0%
	17/05/12 03:57:39 INFO mapreduce.Job:  map 96% reduce 0%
	17/05/12 03:57:40 INFO mapreduce.Job:  map 97% reduce 0%
	17/05/12 03:57:42 INFO mapreduce.Job:  map 99% reduce 0%
	17/05/12 03:57:43 INFO mapreduce.Job:  map 100% reduce 0%
	17/05/12 03:57:44 INFO mapreduce.Job: Job job_1494561292750_0002 completed successfully
	17/05/12 03:57:44 INFO mapreduce.Job: Counters: 31
			File System Counters
					FILE: Number of bytes read=0
					FILE: Number of bytes written=494044
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=339
					HDFS: Number of bytes written=6553600000
					HDFS: Number of read operations=16
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=8
			Job Counters 
					Launched map tasks=4
					Other local map tasks=4
					Total time spent by all maps in occupied slots (ms)=296525
					Total time spent by all reduces in occupied slots (ms)=0
					Total time spent by all map tasks (ms)=296525
					Total vcore-seconds taken by all map tasks=296525
					Total megabyte-seconds taken by all map tasks=303641600
			Map-Reduce Framework
					Map input records=65536000
					Map output records=65536000
					Input split bytes=339
					Spilled Records=0
					Failed Shuffles=0
					Merged Map outputs=0
					GC time elapsed (ms)=1114
					CPU time spent (ms)=110840
					Physical memory (bytes) snapshot=1218793472
					Virtual memory (bytes) snapshot=6268694528
					Total committed heap usage (bytes)=1118306304
			org.apache.hadoop.examples.terasort.TeraGen$Counters
					CHECKSUM=140750829423462787
			File Input Format Counters 
					Bytes Read=0
			File Output Format Counters 
					Bytes Written=6553600000
	
	real    1m33.328s
	user    0m6.682s
	sys     0m0.910s


The result of the time command

	real    1m33.328s
	user    0m6.682s
	sys     0m0.910s

The command and output of hdfs dfs -ls /user/zhou/tgen

	[zhou@ip-172-31-1-194 ~]$ hdfs dfs -ls /user/zhou/tgen
	Found 5 items
	-rw-r--r--   3 zhou zhou          0 2017-05-12 03:57 /user/zhou/tgen/_SUCCESS
	-rw-r--r--   3 zhou zhou 1638400000 2017-05-12 03:57 /user/zhou/tgen/part-m-00000
	-rw-r--r--   3 zhou zhou 1638400000 2017-05-12 03:57 /user/zhou/tgen/part-m-00001
	-rw-r--r--   3 zhou zhou 1638400000 2017-05-12 03:57 /user/zhou/tgen/part-m-00002
	-rw-r--r--   3 zhou zhou 1638400000 2017-05-12 03:57 /user/zhou/tgen/part-m-00003