
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
	[root@ip-172-31-1-96 /]# df -hl
	Filesystem      Size  Used Avail Use% Mounted on
	/dev/xvde       7.9G  650M  6.9G   9% /
	tmpfs           7.4G     0  7.4G   0% /dev/shm
	[root@ip-172-31-1-96 /]# df -Th
	Filesystem     Type   Size  Used Avail Use% Mounted on
	/dev/xvde      ext4   7.9G  650M  6.9G   9% /
	tmpfs          tmpfs  7.4G     0  7.4G   0% /dev/shm
3.
