List the cloud provider you are using

	AWS	
List your instances by their IP address and DNS name

	Private DNS name 							Private ip	
	ip-172-31-1-194.us-west-1.compute.internal	172.31.1.194
	ip-172-31-1-78.us-west-1.compute.internal	172.31.1.78
	ip-172-31-13-75.us-west-1.compute.internal	172.31.13.75
	ip-172-31-10-63.us-west-1.compute.internal	172.31.10.63
	ip-172-31-3-136.us-west-1.compute.internal	172.31.3.136

	Public DNS Name										Public IP
	ec2-54-183-236-31.us-west-1.compute.amazonaws.com	54.183.236.31
	ec2-54-193-68-166.us-west-1.compute.amazonaws.com	54.193.68.166
	ec2-54-215-162-31.us-west-1.compute.amazonaws.com	54.215.162.31
	ec2-52-53-212-165.us-west-1.compute.amazonaws.com	52.53.212.165
	ec2-52-53-156-217.us-west-1.compute.amazonaws.com	52.53.156.217

List the file system capacity for the first node

	[root@ip-172-31-1-194 ~]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        30G  668M   28G   3% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	
	[root@ip-172-31-1-78 ~]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        30G  657M   28G   3% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	
	[root@ip-172-31-10-63 ~]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        30G  661M   28G   3% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	
	[root@ip-172-31-13-75 ~]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        30G  661M   28G   3% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	
	[root@ip-172-31-3-136 ~]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde        30G  656M   28G   3% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm

List the command and output for
	
	[root@ip-172-31-1-194 ~]# yum repolist enabled
	Loaded plugins: fastestmirror, presto
	base                                                                                                                                             | 3.7 kB     00:00     
	base/primary_db                                                                                                                                  | 4.7 MB     00:00     
	extras                                                                                                                                           | 3.4 kB     00:00     
	extras/primary_db                                                                                                                                |  37 kB     00:00     
	updates                                                                                                                                          | 3.4 kB     00:00     
	updates/primary_db                                                                                                                               | 821 kB     00:00     
	repo id                                                                    repo name                                                                              status
	base                                                                       CentOS-6 - Base                                                                        6,706
	extras                                                                     CentOS-6 - Extras                                                                         64
	updates                                                                    CentOS-6 - Updates                                                                       270
	repolist: 7,040

List the /etc/passwd entries for zhou and chen

	[root@ip-172-31-1-194 ~]# cat /etc/passwd |grep zhou
	zhou:x:2800:501::/home/zhou:/bin/bash
	[root@ip-172-31-1-194 ~]# cat /etc/passwd |grep chen
	chen:x:2900:500::/home/chen:/bin/bash

List the /etc/group entries for shanghai and beijing

	[root@ip-172-31-1-194 ~]# cat /etc/group |grep beijing
	beijing:x:501:
	[root@ip-172-31-1-194 ~]# cat /etc/group |grep shanghai
	shanghai:x:500:

