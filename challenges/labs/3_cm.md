The command and output for hdfs dfs -ls /user

	[hdfs@ip-172-31-1-194 root]$ hdfs dfs -ls /user
	Found 7 items
	drwxr-xr-x   - chen   chen            0 2017-05-12 03:26 /user/chen
	drwxrwxrwx   - mapred hadoop          0 2017-05-12 03:20 /user/history
	drwxrwxr-t   - hive   hive            0 2017-05-12 03:21 /user/hive
	drwxrwxr-x   - hue    hue             0 2017-05-12 03:21 /user/hue
	drwxrwxr-x   - impala impala          0 2017-05-12 03:21 /user/impala
	drwxrwxr-x   - oozie  oozie           0 2017-05-12 03:21 /user/oozie
	drwxr-xr-x   - zhou   zhou            0 2017-05-12 03:26 /user/zhou

The command and output from the CM API call ../api/v14/hosts

	[root@ip-172-31-1-194 ~]# curl -u admin:admin 'http://172.31.1.78:7180/api/v14/hosts' 
	{
	"items" : [ {
		"hostId" : "1b6463b0-00a3-4ae3-9a1b-806f7cd6b481",
		"ipAddress" : "172.31.1.194",
		"hostname" : "ip-172-31-1-194.us-west-1.compute.internal",
		"rackId" : "/default",
		"hostUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/hostRedirect/1b6463b0-00a3-4ae3-9a1b-806f7cd6b481",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 4,
		"totalPhysMemBytes" : 15740305408
	}, {
		"hostId" : "58f05579-744e-4615-8d2e-5ab7e00d9993",
		"ipAddress" : "172.31.1.78",
		"hostname" : "ip-172-31-1-78.us-west-1.compute.internal",
		"rackId" : "/default",
		"hostUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/hostRedirect/58f05579-744e-4615-8d2e-5ab7e00d9993",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 4,
		"totalPhysMemBytes" : 15740305408
	}, {
		"hostId" : "e99c441e-7c56-4808-b78f-57c2ffe55688",
		"ipAddress" : "172.31.10.63",
		"hostname" : "ip-172-31-10-63.us-west-1.compute.internal",
		"rackId" : "/default",
		"hostUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/hostRedirect/e99c441e-7c56-4808-b78f-57c2ffe55688",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 4,
		"totalPhysMemBytes" : 15740305408
	}, {
		"hostId" : "1dd8730d-cbd8-43cd-99d5-7d288e44f396",
		"ipAddress" : "172.31.13.75",
		"hostname" : "ip-172-31-13-75.us-west-1.compute.internal",
		"rackId" : "/default",
		"hostUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/hostRedirect/1dd8730d-cbd8-43cd-99d5-7d288e44f396",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 4,
		"totalPhysMemBytes" : 15740305408
	}, {
		"hostId" : "8cb4383d-532b-42e4-984e-9c6e33ccd84a",
		"ipAddress" : "172.31.3.136",
		"hostname" : "ip-172-31-3-136.us-west-1.compute.internal",
		"rackId" : "/default",
		"hostUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/hostRedirect/8cb4383d-532b-42e4-984e-9c6e33ccd84a",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"commissionState" : "COMMISSIONED",
		"numCores" : 4,
		"numPhysicalCores" : 4,
		"totalPhysMemBytes" : 15740305408
	} ]
	}


The command and output from the CM API call ../api/v6/clusters/<githubName>/services

	[root@ip-172-31-1-194 ~]# curl -u admin:admin 'http://172.31.1.78:7180/api/v6/clusters/wk109353794/services
	> '
	{
	"items" : [ {
		"name" : "zookeeper",
		"type" : "ZOOKEEPER",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/zookeeper",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "ZOOKEEPER_CANARY_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "ZOOKEEPER_SERVERS_HEALTHY",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "ZooKeeper"
	}, {
		"name" : "oozie",
		"type" : "OOZIE",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/oozie",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "Oozie"
	}, {
		"name" : "hue",
		"type" : "HUE",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/hue",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "HUE_HUE_SERVERS_HEALTHY",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "Hue"
	}, {
		"name" : "hdfs",
		"type" : "HDFS",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/hdfs",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_CANARY_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_DATA_NODES_HEALTHY",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_FREE_SPACE_REMAINING",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_HA_NAMENODE_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_MISSING_BLOCKS",
		"summary" : "GOOD"
		}, {
		"name" : "HDFS_UNDER_REPLICATED_BLOCKS",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "HDFS"
	}, {
		"name" : "impala",
		"type" : "IMPALA",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/impala",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "IMPALA_ASSIGNMENT_LOCALITY",
		"summary" : "DISABLED"
		}, {
		"name" : "IMPALA_CATALOGSERVER_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "IMPALA_IMPALADS_HEALTHY",
		"summary" : "GOOD"
		}, {
		"name" : "IMPALA_STATESTORE_HEALTH",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "Impala"
	}, {
		"name" : "yarn",
		"type" : "YARN",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/yarn",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "YARN_JOBHISTORY_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "YARN_NODE_MANAGERS_HEALTHY",
		"summary" : "GOOD"
		}, {
		"name" : "YARN_RESOURCEMANAGERS_HEALTH",
		"summary" : "GOOD"
		}, {
		"name" : "YARN_USAGE_AGGREGATION_HEALTH",
		"summary" : "DISABLED"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "YARN (MR2 Included)"
	}, {
		"name" : "hive",
		"type" : "HIVE",
		"clusterRef" : {
		"clusterName" : "cluster"
		},
		"serviceUrl" : "http://ip-172-31-1-78.us-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
		"serviceState" : "STARTED",
		"healthSummary" : "GOOD",
		"healthChecks" : [ {
		"name" : "HIVE_HIVEMETASTORES_HEALTHY",
		"summary" : "GOOD"
		}, {
		"name" : "HIVE_HIVESERVER2S_HEALTHY",
		"summary" : "GOOD"
		} ],
		"configStalenessStatus" : "FRESH",
		"clientConfigStalenessStatus" : "FRESH",
		"maintenanceMode" : false,
		"maintenanceOwners" : [ ],
		"displayName" : "Hive"
	} ]
	}

