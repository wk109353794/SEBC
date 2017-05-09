Create an end-user Linux account named with your GitHub handle 

	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -mkdir /user/wk109353794
	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -chown -R wk109353794:wk109353794 /user/wk109353794 
	[hdfs@ip-172-31-1-96 ~]$ hdfs dfs -ls /user/
	Found 7 items
	drwx------   - hdfs        supergroup           0 2017-05-09 08:37 /user/hdfs
	drwxrwxrwx   - mapred      hadoop               0 2017-05-09 06:14 /user/history
	drwxrwxr-t   - hive        hive                 0 2017-05-09 06:23 /user/hive
	drwxrwxr-x   - hue         hue                  0 2017-05-09 06:24 /user/hue
	drwxrwxr-x   - oozie       oozie                0 2017-05-09 06:29 /user/oozie
	drwxr-xr-x   - root        root                 0 2017-05-09 08:09 /user/root
	drwxr-xr-x   - wk109353794 wk109353794          0 2017-05-09 09:39 /user/wk109353794

Create a 10 GB file using teragen

	[wk109353794@ip-172-31-1-96 ~]$ time -p hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapred.map.tasks=4 107374182 /user/wk109353794/output
	17/05/09 09:54:02 INFO terasort.TeraSort: Generating 107374182 using 4
	17/05/09 09:54:02 INFO mapreduce.JobSubmitter: number of splits:4
	17/05/09 09:54:02 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
	17/05/09 09:54:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494323284139_0001
	17/05/09 09:54:02 INFO impl.YarnClientImpl: Submitted application application_1494323284139_0001
	17/05/09 09:54:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-1-96.us-west-1.compute.internal:8088/proxy/application_1494323284139_0001/
	17/05/09 09:54:02 INFO mapreduce.Job: Running job: job_1494323284139_0001
	17/05/09 09:54:10 INFO mapreduce.Job: Job job_1494323284139_0001 running in uber mode : false
	17/05/09 09:54:10 INFO mapreduce.Job:  map 0% reduce 0%
	17/05/09 09:54:22 INFO mapreduce.Job:  map 3% reduce 0%
	17/05/09 09:54:23 INFO mapreduce.Job:  map 8% reduce 0%
	17/05/09 09:54:25 INFO mapreduce.Job:  map 9% reduce 0%
	17/05/09 09:54:26 INFO mapreduce.Job:  map 12% reduce 0%
	17/05/09 09:54:28 INFO mapreduce.Job:  map 13% reduce 0%
	17/05/09 09:54:29 INFO mapreduce.Job:  map 14% reduce 0%
	17/05/09 09:54:31 INFO mapreduce.Job:  map 15% reduce 0%
	17/05/09 09:54:32 INFO mapreduce.Job:  map 16% reduce 0%
	17/05/09 09:54:34 INFO mapreduce.Job:  map 17% reduce 0%
	17/05/09 09:54:35 INFO mapreduce.Job:  map 18% reduce 0%
	17/05/09 09:54:37 INFO mapreduce.Job:  map 19% reduce 0%
	17/05/09 09:54:38 INFO mapreduce.Job:  map 21% reduce 0%
	17/05/09 09:54:41 INFO mapreduce.Job:  map 22% reduce 0%
	17/05/09 09:54:43 INFO mapreduce.Job:  map 23% reduce 0%
	17/05/09 09:54:44 INFO mapreduce.Job:  map 25% reduce 0%
	17/05/09 09:54:47 INFO mapreduce.Job:  map 27% reduce 0%
	17/05/09 09:54:50 INFO mapreduce.Job:  map 29% reduce 0%
	17/05/09 09:54:53 INFO mapreduce.Job:  map 31% reduce 0%
	17/05/09 09:54:56 INFO mapreduce.Job:  map 33% reduce 0%
	17/05/09 09:54:59 INFO mapreduce.Job:  map 35% reduce 0%
	17/05/09 09:55:03 INFO mapreduce.Job:  map 37% reduce 0%
	17/05/09 09:55:06 INFO mapreduce.Job:  map 38% reduce 0%
	17/05/09 09:55:08 INFO mapreduce.Job:  map 39% reduce 0%
	17/05/09 09:55:09 INFO mapreduce.Job:  map 40% reduce 0%
	17/05/09 09:55:11 INFO mapreduce.Job:  map 41% reduce 0%
	17/05/09 09:55:12 INFO mapreduce.Job:  map 42% reduce 0%
	17/05/09 09:55:14 INFO mapreduce.Job:  map 43% reduce 0%
	17/05/09 09:55:15 INFO mapreduce.Job:  map 44% reduce 0%
	17/05/09 09:55:17 INFO mapreduce.Job:  map 45% reduce 0%
	17/05/09 09:55:18 INFO mapreduce.Job:  map 46% reduce 0%
	17/05/09 09:55:20 INFO mapreduce.Job:  map 47% reduce 0%
	17/05/09 09:55:21 INFO mapreduce.Job:  map 48% reduce 0%
	17/05/09 09:55:23 INFO mapreduce.Job:  map 49% reduce 0%
	17/05/09 09:55:24 INFO mapreduce.Job:  map 50% reduce 0%
	17/05/09 09:55:26 INFO mapreduce.Job:  map 51% reduce 0%
	17/05/09 09:55:27 INFO mapreduce.Job:  map 52% reduce 0%
	17/05/09 09:55:29 INFO mapreduce.Job:  map 53% reduce 0%
	17/05/09 09:55:30 INFO mapreduce.Job:  map 54% reduce 0%
	17/05/09 09:55:32 INFO mapreduce.Job:  map 55% reduce 0%
	17/05/09 09:55:33 INFO mapreduce.Job:  map 56% reduce 0%
	17/05/09 09:55:35 INFO mapreduce.Job:  map 57% reduce 0%
	17/05/09 09:55:36 INFO mapreduce.Job:  map 58% reduce 0%
	17/05/09 09:55:38 INFO mapreduce.Job:  map 59% reduce 0%
	17/05/09 09:55:39 INFO mapreduce.Job:  map 60% reduce 0%
	17/05/09 09:55:41 INFO mapreduce.Job:  map 61% reduce 0%
	17/05/09 09:55:42 INFO mapreduce.Job:  map 62% reduce 0%
	17/05/09 09:55:44 INFO mapreduce.Job:  map 63% reduce 0%
	17/05/09 09:55:45 INFO mapreduce.Job:  map 64% reduce 0%
	17/05/09 09:55:47 INFO mapreduce.Job:  map 65% reduce 0%
	17/05/09 09:55:48 INFO mapreduce.Job:  map 66% reduce 0%
	17/05/09 09:55:50 INFO mapreduce.Job:  map 67% reduce 0%
	17/05/09 09:55:51 INFO mapreduce.Job:  map 68% reduce 0%
	17/05/09 09:55:53 INFO mapreduce.Job:  map 69% reduce 0%
	17/05/09 09:55:54 INFO mapreduce.Job:  map 70% reduce 0%
	17/05/09 09:55:56 INFO mapreduce.Job:  map 71% reduce 0%
	17/05/09 09:55:57 INFO mapreduce.Job:  map 72% reduce 0%
	17/05/09 09:55:59 INFO mapreduce.Job:  map 73% reduce 0%
	17/05/09 09:56:00 INFO mapreduce.Job:  map 74% reduce 0%
	17/05/09 09:56:02 INFO mapreduce.Job:  map 75% reduce 0%
	17/05/09 09:56:03 INFO mapreduce.Job:  map 76% reduce 0%
	17/05/09 09:56:05 INFO mapreduce.Job:  map 77% reduce 0%
	17/05/09 09:56:06 INFO mapreduce.Job:  map 78% reduce 0%
	17/05/09 09:56:08 INFO mapreduce.Job:  map 79% reduce 0%
	17/05/09 09:56:09 INFO mapreduce.Job:  map 80% reduce 0%
	17/05/09 09:56:12 INFO mapreduce.Job:  map 81% reduce 0%
	17/05/09 09:56:13 INFO mapreduce.Job:  map 82% reduce 0%
	17/05/09 09:56:15 INFO mapreduce.Job:  map 83% reduce 0%
	17/05/09 09:56:16 INFO mapreduce.Job:  map 84% reduce 0%
	17/05/09 09:56:18 INFO mapreduce.Job:  map 85% reduce 0%
	17/05/09 09:56:19 INFO mapreduce.Job:  map 86% reduce 0%
	17/05/09 09:56:21 INFO mapreduce.Job:  map 87% reduce 0%
	17/05/09 09:56:22 INFO mapreduce.Job:  map 88% reduce 0%
	17/05/09 09:56:24 INFO mapreduce.Job:  map 90% reduce 0%
	17/05/09 09:56:25 INFO mapreduce.Job:  map 91% reduce 0%
	17/05/09 09:56:28 INFO mapreduce.Job:  map 92% reduce 0%
	17/05/09 09:56:30 INFO mapreduce.Job:  map 93% reduce 0%
	17/05/09 09:56:31 INFO mapreduce.Job:  map 94% reduce 0%
	17/05/09 09:56:33 INFO mapreduce.Job:  map 95% reduce 0%
	17/05/09 09:56:34 INFO mapreduce.Job:  map 96% reduce 0%
	17/05/09 09:56:36 INFO mapreduce.Job:  map 97% reduce 0%
	17/05/09 09:56:37 INFO mapreduce.Job:  map 98% reduce 0%
	17/05/09 09:56:40 INFO mapreduce.Job:  map 100% reduce 0%
	17/05/09 09:56:41 INFO mapreduce.Job: Job job_1494323284139_0001 completed successfully
	17/05/09 09:56:41 INFO mapreduce.Job: Counters: 31
			File System Counters
					FILE: Number of bytes read=0
					FILE: Number of bytes written=514220
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=344
					HDFS: Number of bytes written=10737418200
					HDFS: Number of read operations=16
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=8
			Job Counters 
					Launched map tasks=4
					Other local map tasks=4
					Total time spent by all maps in occupied slots (ms)=583990
					Total time spent by all reduces in occupied slots (ms)=0
					Total time spent by all map tasks (ms)=583990
					Total vcore-seconds taken by all map tasks=583990
					Total megabyte-seconds taken by all map tasks=598005760
			Map-Reduce Framework
					Map input records=107374182
					Map output records=107374182
					Input split bytes=344
					Spilled Records=0
					Failed Shuffles=0
					Merged Map outputs=0
					GC time elapsed (ms)=1944
					CPU time spent (ms)=168230
					Physical memory (bytes) snapshot=942305280
					Virtual memory (bytes) snapshot=6255038464
					Total committed heap usage (bytes)=825753600
			org.apache.hadoop.examples.terasort.TeraGen$Counters
					CHECKSUM=230593859918397906
			File Input Format Counters 
					Bytes Read=0
			File Output Format Counters 
					Bytes Written=10737418200
	real 163.06
	user 6.04
	sys 0.76

Run the terasort command on this file 

	[wk109353794@ip-172-31-1-96 ~]$ time -p hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort -Dmapred.reduce.tasks=6 \
	> /user/wk109353794/output /user/wk109353794/
	17/05/09 10:15:48 INFO terasort.TeraSort: starting
	17/05/09 10:15:49 INFO input.FileInputFormat: Total input paths to process : 4
	Spent 302ms computing base-splits.
	Spent 6ms computing TeraScheduler splits.
	Computing input splits took 309ms
	Sampling 10 splits of 320
	Making 6 from 100000 sampled records
	Computing parititions took 985ms
	Spent 1297ms computing partitions.
	17/05/09 10:15:51 INFO mapreduce.JobSubmitter: number of splits:320
	17/05/09 10:15:51 INFO Configuration.deprecation: mapred.reduce.tasks is deprecated. Instead, use mapreduce.job.reduces
	17/05/09 10:15:51 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494323284139_0002
	17/05/09 10:15:52 INFO impl.YarnClientImpl: Submitted application application_1494323284139_0002
	17/05/09 10:15:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-1-96.us-west-1.compute.internal:8088/proxy/application_1494323284139_0002/
	17/05/09 10:15:52 INFO mapreduce.Job: Running job: job_1494323284139_0002
	17/05/09 10:15:59 INFO mapreduce.Job: Job job_1494323284139_0002 running in uber mode : false
	17/05/09 10:15:59 INFO mapreduce.Job:  map 0% reduce 0%
	17/05/09 10:16:11 INFO mapreduce.Job:  map 2% reduce 0%
	17/05/09 10:16:13 INFO mapreduce.Job:  map 3% reduce 0%
	17/05/09 10:16:21 INFO mapreduce.Job:  map 4% reduce 0%
	17/05/09 10:16:22 INFO mapreduce.Job:  map 5% reduce 0%
	17/05/09 10:16:31 INFO mapreduce.Job:  map 6% reduce 0%
	17/05/09 10:16:32 INFO mapreduce.Job:  map 7% reduce 0%
	17/05/09 10:16:37 INFO mapreduce.Job:  map 8% reduce 0%
	17/05/09 10:16:42 INFO mapreduce.Job:  map 9% reduce 0%
	17/05/09 10:16:44 INFO mapreduce.Job:  map 10% reduce 0%
	17/05/09 10:16:51 INFO mapreduce.Job:  map 11% reduce 0%
	17/05/09 10:16:53 INFO mapreduce.Job:  map 12% reduce 0%
	17/05/09 10:17:00 INFO mapreduce.Job:  map 13% reduce 0%
	17/05/09 10:17:03 INFO mapreduce.Job:  map 14% reduce 0%
	17/05/09 10:17:09 INFO mapreduce.Job:  map 15% reduce 0%
	17/05/09 10:17:13 INFO mapreduce.Job:  map 16% reduce 0%
	17/05/09 10:17:16 INFO mapreduce.Job:  map 17% reduce 0%
	17/05/09 10:17:23 INFO mapreduce.Job:  map 18% reduce 0%
	17/05/09 10:17:25 INFO mapreduce.Job:  map 19% reduce 0%
	17/05/09 10:17:30 INFO mapreduce.Job:  map 20% reduce 0%
	17/05/09 10:17:34 INFO mapreduce.Job:  map 21% reduce 0%
	17/05/09 10:17:36 INFO mapreduce.Job:  map 22% reduce 0%
	17/05/09 10:17:43 INFO mapreduce.Job:  map 23% reduce 0%
	17/05/09 10:17:46 INFO mapreduce.Job:  map 24% reduce 0%
	17/05/09 10:17:52 INFO mapreduce.Job:  map 25% reduce 0%
	17/05/09 10:17:54 INFO mapreduce.Job:  map 26% reduce 0%
	17/05/09 10:18:00 INFO mapreduce.Job:  map 27% reduce 0%
	17/05/09 10:18:03 INFO mapreduce.Job:  map 28% reduce 0%
	17/05/09 10:18:06 INFO mapreduce.Job:  map 29% reduce 0%
	17/05/09 10:18:12 INFO mapreduce.Job:  map 30% reduce 0%
	17/05/09 10:18:15 INFO mapreduce.Job:  map 31% reduce 0%
	17/05/09 10:18:20 INFO mapreduce.Job:  map 32% reduce 0%
	17/05/09 10:18:24 INFO mapreduce.Job:  map 33% reduce 0%
	17/05/09 10:18:30 INFO mapreduce.Job:  map 34% reduce 0%
	17/05/09 10:18:34 INFO mapreduce.Job:  map 35% reduce 0%
	17/05/09 10:18:35 INFO mapreduce.Job:  map 36% reduce 0%
	17/05/09 10:18:41 INFO mapreduce.Job:  map 37% reduce 0%
	17/05/09 10:18:44 INFO mapreduce.Job:  map 38% reduce 0%
	17/05/09 10:18:51 INFO mapreduce.Job:  map 39% reduce 0%
	17/05/09 10:18:54 INFO mapreduce.Job:  map 40% reduce 0%
	17/05/09 10:18:56 INFO mapreduce.Job:  map 41% reduce 0%
	17/05/09 10:19:01 INFO mapreduce.Job:  map 42% reduce 0%
	17/05/09 10:19:04 INFO mapreduce.Job:  map 43% reduce 0%
	17/05/09 10:19:11 INFO mapreduce.Job:  map 44% reduce 0%
	17/05/09 10:19:14 INFO mapreduce.Job:  map 45% reduce 0%
	17/05/09 10:19:19 INFO mapreduce.Job:  map 46% reduce 0%
	17/05/09 10:19:23 INFO mapreduce.Job:  map 47% reduce 0%
	17/05/09 10:19:26 INFO mapreduce.Job:  map 48% reduce 0%
	17/05/09 10:19:31 INFO mapreduce.Job:  map 49% reduce 0%
	17/05/09 10:19:34 INFO mapreduce.Job:  map 50% reduce 0%
	17/05/09 10:19:40 INFO mapreduce.Job:  map 51% reduce 0%
	17/05/09 10:19:43 INFO mapreduce.Job:  map 52% reduce 0%
	17/05/09 10:19:49 INFO mapreduce.Job:  map 53% reduce 0%
	17/05/09 10:19:54 INFO mapreduce.Job:  map 54% reduce 0%
	17/05/09 10:19:58 INFO mapreduce.Job:  map 55% reduce 0%
	17/05/09 10:20:00 INFO mapreduce.Job:  map 56% reduce 0%
	17/05/09 10:20:04 INFO mapreduce.Job:  map 57% reduce 0%
	17/05/09 10:20:10 INFO mapreduce.Job:  map 58% reduce 0%
	17/05/09 10:20:15 INFO mapreduce.Job:  map 59% reduce 0%
	17/05/09 10:20:18 INFO mapreduce.Job:  map 60% reduce 0%
	17/05/09 10:20:24 INFO mapreduce.Job:  map 61% reduce 0%
	17/05/09 10:20:25 INFO mapreduce.Job:  map 62% reduce 0%
	17/05/09 10:20:30 INFO mapreduce.Job:  map 63% reduce 0%
	17/05/09 10:20:36 INFO mapreduce.Job:  map 64% reduce 0%
	17/05/09 10:20:38 INFO mapreduce.Job:  map 65% reduce 0%
	17/05/09 10:20:44 INFO mapreduce.Job:  map 66% reduce 0%
	17/05/09 10:20:47 INFO mapreduce.Job:  map 67% reduce 0%
	17/05/09 10:20:52 INFO mapreduce.Job:  map 68% reduce 0%
	17/05/09 10:20:56 INFO mapreduce.Job:  map 69% reduce 0%
	17/05/09 10:20:59 INFO mapreduce.Job:  map 70% reduce 0%
	17/05/09 10:21:05 INFO mapreduce.Job:  map 71% reduce 0%
	17/05/09 10:21:07 INFO mapreduce.Job:  map 72% reduce 0%
	17/05/09 10:21:12 INFO mapreduce.Job:  map 73% reduce 0%
	17/05/09 10:21:17 INFO mapreduce.Job:  map 74% reduce 0%
	17/05/09 10:21:23 INFO mapreduce.Job:  map 75% reduce 0%
	17/05/09 10:21:25 INFO mapreduce.Job:  map 76% reduce 0%
	17/05/09 10:21:27 INFO mapreduce.Job:  map 77% reduce 0%
	17/05/09 10:21:35 INFO mapreduce.Job:  map 78% reduce 0%
	17/05/09 10:21:37 INFO mapreduce.Job:  map 79% reduce 0%
	17/05/09 10:21:43 INFO mapreduce.Job:  map 80% reduce 0%
	17/05/09 10:21:46 INFO mapreduce.Job:  map 81% reduce 0%
	17/05/09 10:21:49 INFO mapreduce.Job:  map 82% reduce 0%
	17/05/09 10:21:59 INFO mapreduce.Job:  map 82% reduce 6%
	17/05/09 10:22:01 INFO mapreduce.Job:  map 82% reduce 7%
	17/05/09 10:22:02 INFO mapreduce.Job:  map 82% reduce 8%
	17/05/09 10:22:03 INFO mapreduce.Job:  map 82% reduce 11%
	17/05/09 10:22:04 INFO mapreduce.Job:  map 82% reduce 12%
	17/05/09 10:22:05 INFO mapreduce.Job:  map 83% reduce 12%
	17/05/09 10:22:07 INFO mapreduce.Job:  map 83% reduce 13%
	17/05/09 10:22:09 INFO mapreduce.Job:  map 83% reduce 15%
	17/05/09 10:22:10 INFO mapreduce.Job:  map 83% reduce 16%
	17/05/09 10:22:12 INFO mapreduce.Job:  map 83% reduce 17%
	17/05/09 10:22:13 INFO mapreduce.Job:  map 83% reduce 18%
	17/05/09 10:22:15 INFO mapreduce.Job:  map 83% reduce 19%
	17/05/09 10:22:16 INFO mapreduce.Job:  map 84% reduce 19%
	17/05/09 10:22:23 INFO mapreduce.Job:  map 85% reduce 19%
	17/05/09 10:22:30 INFO mapreduce.Job:  map 86% reduce 19%
	17/05/09 10:22:36 INFO mapreduce.Job:  map 87% reduce 19%
	17/05/09 10:22:43 INFO mapreduce.Job:  map 88% reduce 19%
	17/05/09 10:22:51 INFO mapreduce.Job:  map 88% reduce 20%
	17/05/09 10:22:56 INFO mapreduce.Job:  map 89% reduce 20%
	17/05/09 10:23:02 INFO mapreduce.Job:  map 90% reduce 20%
	17/05/09 10:23:09 INFO mapreduce.Job:  map 91% reduce 20%
	17/05/09 10:23:16 INFO mapreduce.Job:  map 92% reduce 20%
	17/05/09 10:23:23 INFO mapreduce.Job:  map 93% reduce 20%
	17/05/09 10:23:25 INFO mapreduce.Job:  map 93% reduce 21%
	17/05/09 10:23:36 INFO mapreduce.Job:  map 94% reduce 21%
	17/05/09 10:23:43 INFO mapreduce.Job:  map 95% reduce 21%
	17/05/09 10:23:49 INFO mapreduce.Job:  map 96% reduce 21%
	17/05/09 10:23:56 INFO mapreduce.Job:  map 97% reduce 21%
	17/05/09 10:24:03 INFO mapreduce.Job:  map 98% reduce 21%
	17/05/09 10:24:04 INFO mapreduce.Job:  map 98% reduce 22%
	17/05/09 10:24:15 INFO mapreduce.Job:  map 99% reduce 22%
	17/05/09 10:24:21 INFO mapreduce.Job:  map 100% reduce 22%
	17/05/09 10:24:27 INFO mapreduce.Job:  map 100% reduce 23%
	17/05/09 10:24:28 INFO mapreduce.Job:  map 100% reduce 34%
	17/05/09 10:24:29 INFO mapreduce.Job:  map 100% reduce 40%
	17/05/09 10:24:30 INFO mapreduce.Job:  map 100% reduce 45%
	17/05/09 10:24:31 INFO mapreduce.Job:  map 100% reduce 49%
	17/05/09 10:24:32 INFO mapreduce.Job:  map 100% reduce 50%
	17/05/09 10:24:34 INFO mapreduce.Job:  map 100% reduce 54%
	17/05/09 10:24:36 INFO mapreduce.Job:  map 100% reduce 55%
	17/05/09 10:24:37 INFO mapreduce.Job:  map 100% reduce 56%
	17/05/09 10:24:38 INFO mapreduce.Job:  map 100% reduce 58%
	17/05/09 10:24:40 INFO mapreduce.Job:  map 100% reduce 60%
	17/05/09 10:24:41 INFO mapreduce.Job:  map 100% reduce 61%
	17/05/09 10:24:43 INFO mapreduce.Job:  map 100% reduce 63%
	17/05/09 10:24:44 INFO mapreduce.Job:  map 100% reduce 64%
	17/05/09 10:24:45 INFO mapreduce.Job:  map 100% reduce 65%
	17/05/09 10:24:46 INFO mapreduce.Job:  map 100% reduce 67%
	17/05/09 10:24:47 INFO mapreduce.Job:  map 100% reduce 69%
	17/05/09 10:24:48 INFO mapreduce.Job:  map 100% reduce 70%
	17/05/09 10:24:50 INFO mapreduce.Job:  map 100% reduce 72%
	17/05/09 10:24:52 INFO mapreduce.Job:  map 100% reduce 73%
	17/05/09 10:24:53 INFO mapreduce.Job:  map 100% reduce 79%
	17/05/09 10:24:55 INFO mapreduce.Job:  map 100% reduce 85%
	17/05/09 10:24:56 INFO mapreduce.Job:  map 100% reduce 87%
	17/05/09 10:24:58 INFO mapreduce.Job:  map 100% reduce 88%
	17/05/09 10:24:59 INFO mapreduce.Job:  map 100% reduce 89%
	17/05/09 10:25:01 INFO mapreduce.Job:  map 100% reduce 90%
	17/05/09 10:25:02 INFO mapreduce.Job:  map 100% reduce 91%
	17/05/09 10:25:04 INFO mapreduce.Job:  map 100% reduce 92%
	17/05/09 10:25:05 INFO mapreduce.Job:  map 100% reduce 93%
	17/05/09 10:25:08 INFO mapreduce.Job:  map 100% reduce 95%
	17/05/09 10:25:11 INFO mapreduce.Job:  map 100% reduce 96%
	17/05/09 10:25:14 INFO mapreduce.Job:  map 100% reduce 98%
	17/05/09 10:25:17 INFO mapreduce.Job:  map 100% reduce 99%
	17/05/09 10:25:20 INFO mapreduce.Job:  map 100% reduce 100%
	17/05/09 10:25:21 INFO mapreduce.Job: Job job_1494323284139_0002 completed successfully
	17/05/09 10:25:21 INFO mapreduce.Job: Counters: 49
			File System Counters
					FILE: Number of bytes read=4818050516
					FILE: Number of bytes written=9557979351
					FILE: Number of read operations=0
					FILE: Number of large read operations=0
					FILE: Number of write operations=0
					HDFS: Number of bytes read=10737456920
					HDFS: Number of bytes written=10737418200
					HDFS: Number of read operations=978
					HDFS: Number of large read operations=0
					HDFS: Number of write operations=12
			Job Counters 
					Launched map tasks=320
					Launched reduce tasks=6
					Data-local map tasks=320
					Total time spent by all maps in occupied slots (ms)=2562793
					Total time spent by all reduces in occupied slots (ms)=874347
					Total time spent by all map tasks (ms)=2562793
					Total time spent by all reduce tasks (ms)=874347
					Total vcore-seconds taken by all map tasks=2562793
					Total vcore-seconds taken by all reduce tasks=874347
					Total megabyte-seconds taken by all map tasks=2624300032
					Total megabyte-seconds taken by all reduce tasks=895331328
			Map-Reduce Framework
					Map input records=107374182
					Map output records=107374182
					Map output bytes=10952166564
					Map output materialized bytes=4697547721
					Input split bytes=38720
					Combine input records=0
					Combine output records=0
					Reduce input groups=107374182
					Reduce shuffle bytes=4697547721
					Reduce input records=107374182
					Reduce output records=107374182
					Spilled Records=214748364
					Shuffled Maps =1920
					Failed Shuffles=0
					Merged Map outputs=1920
					GC time elapsed (ms)=32126
					CPU time spent (ms)=1526650
					Physical memory (bytes) snapshot=152575053824
					Virtual memory (bytes) snapshot=510130053120
					Total committed heap usage (bytes)=185773588480
			Shuffle Errors
					BAD_ID=0
					CONNECTION=0
					IO_ERROR=0
					WRONG_LENGTH=0
					WRONG_MAP=0
					WRONG_REDUCE=0
			File Input Format Counters 
					Bytes Read=10737418200
			File Output Format Counters 
					Bytes Written=10737418200
	17/05/09 10:25:21 INFO terasort.TeraSort: done
	real 574.69
	user 10.07
	sys 1.07