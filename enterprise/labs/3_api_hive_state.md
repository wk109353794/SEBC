curl statements for start and stop hive

	curl -X POST -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive/commands/start'
	curl -X POST -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive/commands/stop'

curl statements for check command status

	curl -u wk109353794:cloudera 'http://localhost:7180/api/v1/commands/[command id]'

curl statements for check hive status

	curl -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive'

statements output

	[root@ip-172-31-1-96 ~]# curl -X POST -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive/commands/stop' 
	{
	"id" : 598,
	"name" : "Stop",
	"startTime" : "2017-05-10T04:39:50.943Z",
	"active" : true,
	"serviceRef" : {
		"clusterName" : "cluster",
		"serviceName" : "hive"
	}
	}[root@ip-172-31-1-96 ~]# curl -u wk109353794:cloudera 'http://localhost:7180/api/v1/commands/598'         
	{
	"id" : 598,
	"name" : "Stop",
	"startTime" : "2017-05-10T04:39:50.943Z",
	"endTime" : "2017-05-10T04:39:54.878Z",
	"active" : false,
	"success" : true,
	"resultMessage" : "Successfully stopped service.",
	"serviceRef" : {
		"clusterName" : "cluster",
		"serviceName" : "hive"
	},
	"children" : {
		"items" : [ {
		"id" : 599,
		"name" : "Stop",
		"startTime" : "2017-05-10T04:39:50.945Z",
		"endTime" : "2017-05-10T04:39:54.878Z",
		"active" : false,
		"success" : true,
		"resultMessage" : "Successfully stopped process.",
		"serviceRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive"
		},
		"roleRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive",
			"roleName" : "hive-HIVESERVER2-2d0a9371a899499d432e52671b7d65b3"
		}
		}, {
		"id" : 600,
		"name" : "Stop",
		"startTime" : "2017-05-10T04:39:50.947Z",
		"endTime" : "2017-05-10T04:39:54.870Z",
		"active" : false,
		"success" : true,
		"resultMessage" : "Successfully stopped process.",
		"serviceRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive"
		},
		"roleRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive",
			"roleName" : "hive-HIVEMETASTORE-2d0a9371a899499d432e52671b7d65b3"
		}
		} ]
	}
	}

	[root@ip-172-31-1-96 ~]# curl -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive'
	{
	"name" : "hive",
	"type" : "HIVE",
	"clusterRef" : {
		"clusterName" : "cluster"
	},
	"serviceUrl" : "http://ip-172-31-1-96.us-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
	"serviceState" : "STOPPED",
	"healthSummary" : "DISABLED",
	"healthChecks" : [ {
		"name" : "HIVE_HIVEMETASTORES_HEALTHY",
		"summary" : "DISABLED"
	}, {
		"name" : "HIVE_HIVESERVER2S_HEALTHY",
		"summary" : "DISABLED"
	} ],
	"configStale" : false
	}
	[root@ip-172-31-1-96 ~]# curl -X POST -u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive/commands/start'
	{
	"id" : 602,
	"name" : "Start",
	"startTime" : "2017-05-10T04:50:35.919Z",
	"active" : true,
	"serviceRef" : {
		"clusterName" : "cluster",
		"serviceName" : "hive"
	}
	}[root@ip-172-31-1-96 ~]# curl u wk109353794:cloudera 'http://localhost:7180/api/v1/commands/602'                                              
	{
	"id" : 602,
	"name" : "Start",
	"startTime" : "2017-05-10T04:50:35.919Z",
	"endTime" : "2017-05-10T04:50:58.916Z",
	"active" : false,
	"success" : true,
	"resultMessage" : "Successfully started service.",
	"serviceRef" : {
		"clusterName" : "cluster",
		"serviceName" : "hive"
	},
	"children" : {
		"items" : [ {
		"id" : 604,
		"name" : "Start",
		"startTime" : "2017-05-10T04:50:36.016Z",
		"endTime" : "2017-05-10T04:50:58.911Z",
		"active" : false,
		"success" : true,
		"resultMessage" : "Successfully started process.",
		"serviceRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive"
		},
		"roleRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive",
			"roleName" : "hive-HIVEMETASTORE-2d0a9371a899499d432e52671b7d65b3"
		}
		}, {
		"id" : 603,
		"name" : "Start",
		"startTime" : "2017-05-10T04:50:35.939Z",
		"endTime" : "2017-05-10T04:50:58.904Z",
		"active" : false,
		"success" : true,
		"resultMessage" : "Successfully started process.",
		"serviceRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive"
		},
		"roleRef" : {
			"clusterName" : "cluster",
			"serviceName" : "hive",
			"roleName" : "hive-HIVESERVER2-2d0a9371a899499d432e52671b7d65b3"
		}
		} ]
	}
	}[root@ip-172-31-1-96 ~]# curl u wk109353794:cloudera 'http://localhost:7180/api/v1/clusters/wk109353794/services/hive'                       
	{
	"name" : "hive",
	"type" : "HIVE",
	"clusterRef" : {
		"clusterName" : "cluster"
	},
	"serviceUrl" : "http://ip-172-31-1-96.us-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
	"serviceState" : "STARTED",
	"healthSummary" : "GOOD",
	"healthChecks" : [ {
		"name" : "HIVE_HIVEMETASTORES_HEALTHY",
		"summary" : "GOOD"
	}, {
		"name" : "HIVE_HIVESERVER2S_HEALTHY",
		"summary" : "GOOD"
	} ],
	"configStale" : false
	}