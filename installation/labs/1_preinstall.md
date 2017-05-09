
System Configuration Checks
-------
1.Check vm.swappiness on all your nodes
 
	[root@ip-172-31-1-96 /]# cat /proc/sys/vm/swappiness
	60
	[root@ip-172-31-1-96 /]# sudo sysctl vm.swappiness=1
	vm.swappiness = 1
2.Show the mount attributes of your volume(s)

	[root@ip-172-31-1-96 /]# mount
	/dev/xvde on / type ext4 (rw)
	proc on /proc type proc (rw)
	sysfs on /sys type sysfs (rw)
	devpts on /dev/pts type devpts (rw,gid=5,mode=620)
	tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
	none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
	[root@ip-172-31-1-96 /]# df -Th
	Filesystem     Type   Size  Used Avail Use% Mounted on
	/dev/xvde      ext4   7.9G  650M  6.9G   9% /
	tmpfs          tmpfs  7.4G     0  7.4G   0% /dev/shm
3.If you have ext-based volumes, list the reserve space setting 

	null
4.Disable transparent hugepage support

	[root@ip-172-31-1-96 ~]# cat /proc/sys/vm/nr_hugepages 
	0
	[root@ip-172-31-1-96 ~]# grep -i HugePages_Total /proc/meminfo 
	HugePages_Total:       0

5.List your network interface configuration

	[root@ip-172-31-1-96 ~]# ifconfig
	eth0      Link encap:Ethernet  HWaddr 06:25:55:DA:DA:0C  
			inet addr:172.31.1.96  Bcast:172.31.15.255  Mask:255.255.240.0
			inet6 addr: fe80::425:55ff:feda:da0c/64 Scope:Link
			UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
			RX packets:907 errors:0 dropped:0 overruns:0 frame:0
			TX packets:795 errors:0 dropped:0 overruns:0 carrier:0
			collisions:0 txqueuelen:1000 
			RX bytes:70837 (69.1 KiB)  TX bytes:86328 (84.3 KiB)
			Interrupt:24 
	
	lo        Link encap:Local Loopback  
			inet addr:127.0.0.1  Mask:255.0.0.0
			inet6 addr: ::1/128 Scope:Host
			UP LOOPBACK RUNNING  MTU:16436  Metric:1
			RX packets:0 errors:0 dropped:0 overruns:0 frame:0
			TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
			collisions:0 txqueuelen:0 
			RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)
6.Show that forward and reverse host lookups are correctly resolved

For /etc/hosts, use getent

	[root@nn1 ~]# vi /etc/hosts	
	172.31.13.171   nn2.labs.com    nn2
	172.31.1.96     nn1.labs.com    nn1
	172.31.5.179    dn1.labs.com    dn1
	172.31.13.171   dn2.labs.com    dn2
	172.31.1.58     dn3.labs.com    dn3
	127.0.0.1       localhost 

For DNS, use nslookup 
 
	[root@nn1 ~]# nslookup               
	> www.cloudera.com
	Server:         172.31.0.2
	Address:        172.31.0.2#53
	Non-authoritative answer:
	www.cloudera.com        canonical name = aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com.
	Name:   aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com
	Address: 52.52.206.175
	Name:   aem-prod-external-elb-1751714427.us-west-1.elb.amazonaws.com
	Address: 52.52.88.106

6.Show the nscd service is running

	[root@nn1 ~]# service nscd status
	nscd (pid 1057) is running...
	
	[root@nn2 ~]# service nscd status
	nscd (pid 1003) is running...
	
	[root@dn1 ~]# service nscd status
	nscd (pid 1012) is running...
	
	[root@dn2 ~]# service nscd status
	nscd (pid 992) is running...
	
	[root@dn3 ~]# service nscd status
	nscd (pid 994) is running...

7.Show the ntpd service is running

	[root@dn2 ~]# service ntpd status
	ntpd (pid  1123) is running...
	[root@nn1 ~]# service ntpd status
	ntpd (pid  1227) is running...
	[root@nn2 ~]# service ntpd status
	ntpd (pid  1121) is running...
	[root@dn3 ~]# service ntpd status
	ntpd (pid  1112) is running...
	[root@dn2 ~]# service ntpd status
	ntpd (pid  1123) is running...



