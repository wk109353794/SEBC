	{
	"timestamp" : "2017-05-10T04:25:19.248Z",
	"clusters" : [ {
		"name" : "wk109353794",
		"version" : "CDH5",
		"services" : [ {
		"name" : "hdfs",
		"type" : "HDFS",
		"config" : {
			"roleTypeConfigs" : [ {
			"roleType" : "DATANODE",
			"items" : [ {
				"name" : "datanode_java_heapsize",
				"value" : "1073741824"
			}, {
				"name" : "dfs_data_dir_list",
				"value" : "/dfs/dn"
			}, {
				"name" : "dfs_datanode_du_reserved",
				"value" : "3170683699"
			}, {
				"name" : "dfs_datanode_max_locked_memory",
				"value" : "4294967296"
			}, {
				"name" : "rm_cpu_shares",
				"value" : "400"
			}, {
				"name" : "rm_io_weight",
				"value" : "200"
			} ]
			}, {
			"roleType" : "GATEWAY",
			"items" : [ {
				"name" : "dfs_client_use_trash",
				"value" : "true"
			} ]
			}, {
			"roleType" : "JOURNALNODE",
			"items" : [ {
				"name" : "dfs_journalnode_edits_dir",
				"value" : "/dfs/jn"
			} ]
			}, {
			"roleType" : "NAMENODE",
			"items" : [ {
				"name" : "dfs_name_dir_list",
				"value" : "/dfs/nn"
			}, {
				"name" : "dfs_namenode_servicerpc_address",
				"value" : "8022"
			} ]
			}, {
			"roleType" : "SECONDARYNAMENODE",
			"items" : [ {
				"name" : "fs_checkpoint_dir_list",
				"value" : "/dfs/snn"
			} ]
			} ],
			"items" : [ {
			"name" : "dfs_block_size",
			"value" : "33554432"
			}, {
			"name" : "dfs_ha_fencing_cloudera_manager_secret_key",
			"value" : "bJv8xwIPEyYbBzvfyH42FByAi1IMWR"
			}, {
			"name" : "dfs_ha_fencing_methods",
			"value" : "shell(true)"
			}, {
			"name" : "fc_authorization_secret_key",
			"value" : "pFu8D8IxIC4AQeDvQr1biJBRW1lwtc"
			}, {
			"name" : "http_auth_signature_secret",
			"value" : "xQchHbhEawhbpMGezqIwA0zbE3z3Q9"
			}, {
			"name" : "rm_dirty",
			"value" : "false"
			}, {
			"name" : "rm_last_allocation_percentage",
			"value" : "20"
			}, {
			"name" : "zookeeper_service",
			"value" : "zookeeper"
			} ]
		},
		"roles" : [ {
			"name" : "hdfs-BALANCER-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "BALANCER",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hdfs-DATANODE-2d0a9371a899499d432e52671b7d65b3",
			"type" : "DATANODE",
			"hostRef" : {
			"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "eg73czkad8jqj6kqt68f6a7ks"
			} ]
			}
		}, {
			"name" : "hdfs-DATANODE-6816accef44d80e81118421075bf2b43",
			"type" : "DATANODE",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "1zshg25bzqswmaf1rwrmhmd02"
			} ]
			}
		}, {
			"name" : "hdfs-DATANODE-b3f39c9653941ed458a323dc32878b29",
			"type" : "DATANODE",
			"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "dbb5ledoopvp9nnc5ae6ku5gw"
			} ]
			}
		}, {
			"name" : "hdfs-FAILOVERCONTROLLER-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "FAILOVERCONTROLLER",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "3blraolt04xkgulvnqov3v8zc"
			} ]
			}
		}, {
			"name" : "hdfs-FAILOVERCONTROLLER-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "FAILOVERCONTROLLER",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "awcpc0w6hw99en7t2akkb7ci5"
			} ]
			}
		}, {
			"name" : "hdfs-GATEWAY-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hdfs-HTTPFS-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "HTTPFS",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "2tor7vhaarvg1olnof1z69fyo"
			} ]
			}
		}, {
			"name" : "hdfs-JOURNALNODE-6816accef44d80e81118421075bf2b43",
			"type" : "JOURNALNODE",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "3b3x2ojo2attaa74jpqhbzmrq"
			} ]
			}
		}, {
			"name" : "hdfs-JOURNALNODE-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "JOURNALNODE",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "1sk18bbbbr480t6fl200lu2cm"
			} ]
			}
		}, {
			"name" : "hdfs-JOURNALNODE-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "JOURNALNODE",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "5m3g2f5g56l7nc185xhnfrv6z"
			} ]
			}
		}, {
			"name" : "hdfs-NAMENODE-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "NAMENODE",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "autofailover_enabled",
				"value" : "true"
			}, {
				"name" : "dfs_federation_namenode_nameservice",
				"value" : "nameservice1"
			}, {
				"name" : "dfs_namenode_quorum_journal_name",
				"value" : "nameservice1"
			}, {
				"name" : "namenode_id",
				"value" : "41"
			}, {
				"name" : "role_jceks_password",
				"value" : "5kdf9iwh8l3nzv07cj7taed73"
			} ]
			}
		}, {
			"name" : "hdfs-NAMENODE-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "NAMENODE",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "autofailover_enabled",
				"value" : "true"
			}, {
				"name" : "dfs_federation_namenode_nameservice",
				"value" : "nameservice1"
			}, {
				"name" : "dfs_namenode_quorum_journal_name",
				"value" : "nameservice1"
			}, {
				"name" : "namenode_id",
				"value" : "62"
			}, {
				"name" : "role_jceks_password",
				"value" : "dwzxop1kovapjdqzwx9qcec8j"
			} ]
			}
		} ],
		"displayName" : "HDFS"
		}, {
		"name" : "zookeeper",
		"type" : "ZOOKEEPER",
		"config" : {
			"roleTypeConfigs" : [ ],
			"items" : [ ]
		},
		"roles" : [ {
			"name" : "zookeeper-SERVER-6816accef44d80e81118421075bf2b43",
			"type" : "SERVER",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "66nl56xm3l65q3yomir6y0yom"
			}, {
				"name" : "serverId",
				"value" : "1"
			} ]
			}
		}, {
			"name" : "zookeeper-SERVER-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "SERVER",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "bi1qohlcxqdt8eqnk0expnkup"
			}, {
				"name" : "serverId",
				"value" : "3"
			} ]
			}
		}, {
			"name" : "zookeeper-SERVER-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "SERVER",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "1uiumz79lru83j1yink0fazca"
			}, {
				"name" : "serverId",
				"value" : "2"
			} ]
			}
		} ],
		"displayName" : "ZooKeeper"
		}, {
		"name" : "yarn",
		"type" : "YARN",
		"config" : {
			"roleTypeConfigs" : [ {
			"roleType" : "GATEWAY",
			"items" : [ {
				"name" : "mapred_reduce_tasks",
				"value" : "6"
			}, {
				"name" : "mapred_submit_replication",
				"value" : "1"
			}, {
				"name" : "mapreduce_map_memory_mb",
				"value" : "500"
			}, {
				"name" : "mapreduce_reduce_memory_mb",
				"value" : "1024"
			} ]
			}, {
			"roleType" : "NODEMANAGER",
			"items" : [ {
				"name" : "node_manager_java_heapsize",
				"value" : "52428800"
			}, {
				"name" : "yarn_nodemanager_heartbeat_interval_ms",
				"value" : "100"
			}, {
				"name" : "yarn_nodemanager_local_dirs",
				"value" : "/yarn/nm"
			}, {
				"name" : "yarn_nodemanager_log_dirs",
				"value" : "/yarn/container-logs"
			}, {
				"name" : "yarn_nodemanager_resource_cpu_vcores",
				"value" : "4"
			}, {
				"name" : "yarn_nodemanager_resource_memory_mb",
				"value" : "1024"
			} ]
			}, {
			"roleType" : "RESOURCEMANAGER",
			"items" : [ {
				"name" : "yarn_scheduler_maximum_allocation_mb",
				"value" : "5120"
			}, {
				"name" : "yarn_scheduler_maximum_allocation_vcores",
				"value" : "3"
			} ]
			} ],
			"items" : [ {
			"name" : "hdfs_service",
			"value" : "hdfs"
			}, {
			"name" : "rm_dirty",
			"value" : "false"
			}, {
			"name" : "rm_last_allocation_percentage",
			"value" : "80"
			}, {
			"name" : "yarn_fs_scheduled_allocations",
			"value" : "{\"defaultFairSharePreemptionThreshold\":null,\"defaultFairSharePreemptionTimeout\":null,\"defaultMinSharePreemptionTimeout\":null,\"defaultQueueSchedulingPolicy\":\"drf\",\"queueMaxAMShareDefault\":null,\"queueMaxAppsDefault\":null,\"queuePlacementRules\":[{\"create\":true,\"name\":\"specified\",\"queue\":null,\"rules\":null},{\"create\":null,\"name\":\"nestedUserQueue\",\"queue\":null,\"rules\":[{\"create\":true,\"name\":\"default\",\"queue\":\"users\",\"rules\":null}]},{\"create\":null,\"name\":\"default\",\"queue\":null,\"rules\":null}],\"queues\":[{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\" \",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"root\",\"queues\":[{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\"*\",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"default\",\"queues\":[],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":{\"memory\":3072,\"vcores\":2},\"maxRunningApps\":null,\"minResources\":{\"memory\":1024,\"vcores\":1},\"scheduleName\":\"default\",\"weight\":1.0}],\"schedulingPolicy\":\"drf\",\"type\":null},{\"aclAdministerApps\":\"*\",\"aclSubmitApps\":\"*\",\"allowPreemptionFrom\":null,\"fairSharePreemptionThreshold\":null,\"fairSharePreemptionTimeout\":null,\"minSharePreemptionTimeout\":null,\"name\":\"users\",\"queues\":[],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":{\"memory\":9216,\"vcores\":9},\"maxRunningApps\":null,\"minResources\":{\"memory\":3072,\"vcores\":3},\"scheduleName\":\"default\",\"weight\":4.0}],\"schedulingPolicy\":\"drf\",\"type\":\"parent\"}],\"schedulablePropertiesList\":[{\"impalaDefaultQueryMemLimit\":null,\"impalaDefaultQueryOptions\":null,\"impalaMaxMemory\":null,\"impalaMaxQueuedQueries\":null,\"impalaMaxRunningQueries\":null,\"impalaQueueTimeout\":null,\"maxAMShare\":null,\"maxResources\":null,\"maxRunningApps\":null,\"minResources\":null,\"scheduleName\":\"default\",\"weight\":1.0}],\"schedulingPolicy\":\"drf\",\"type\":null}],\"userMaxAppsDefault\":null,\"users\":[]}"
			}, {
			"name" : "yarn_service_cgroups",
			"value" : "false"
			}, {
			"name" : "yarn_service_lce_always",
			"value" : "false"
			}, {
			"name" : "zk_authorization_secret_key",
			"value" : "Wb5fyGZZPFFi6KuQnADEStPgiSy9bo"
			}, {
			"name" : "zookeeper_service",
			"value" : "zookeeper"
			} ]
		},
		"roles" : [ {
			"name" : "yarn-GATEWAY-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "yarn-JOBHISTORY-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "JOBHISTORY",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "8i22a544pgs2gcuyd0jasg0pj"
			} ]
			}
		}, {
			"name" : "yarn-NODEMANAGER-2d0a9371a899499d432e52671b7d65b3",
			"type" : "NODEMANAGER",
			"hostRef" : {
			"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "1qvjvp9gn3tz3vtz7ffbux89l"
			} ]
			}
		}, {
			"name" : "yarn-NODEMANAGER-6816accef44d80e81118421075bf2b43",
			"type" : "NODEMANAGER",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "4dcl82a6zs54hg2qv9chnusor"
			} ]
			}
		}, {
			"name" : "yarn-NODEMANAGER-b3f39c9653941ed458a323dc32878b29",
			"type" : "NODEMANAGER",
			"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "8aklbklzdqiltia6tuim2mpmk"
			} ]
			}
		}, {
			"name" : "yarn-RESOURCEMANAGER-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "RESOURCEMANAGER",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ {
				"name" : "rm_id",
				"value" : "77"
			}, {
				"name" : "role_jceks_password",
				"value" : "cjrdugn3ih52ulgsczexqoezl"
			} ]
			}
		}, {
			"name" : "yarn-RESOURCEMANAGER-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "RESOURCEMANAGER",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ {
				"name" : "rm_id",
				"value" : "78"
			}, {
				"name" : "role_jceks_password",
				"value" : "odpbq5h5rtcvcqv90egsf0fs"
			} ]
			}
		} ],
		"displayName" : "YARN (MR2 Included)"
		}, {
		"name" : "hive",
		"type" : "HIVE",
		"config" : {
			"roleTypeConfigs" : [ {
			"roleType" : "HIVEMETASTORE",
			"items" : [ {
				"name" : "hive_metastore_java_heapsize",
				"value" : "52428800"
			} ]
			}, {
			"roleType" : "HIVESERVER2",
			"items" : [ {
				"name" : "hiveserver2_java_heapsize",
				"value" : "52428800"
			}, {
				"name" : "hiveserver2_spark_driver_memory",
				"value" : "966367641"
			}, {
				"name" : "hiveserver2_spark_executor_cores",
				"value" : "4"
			}, {
				"name" : "hiveserver2_spark_executor_memory",
				"value" : "912680550"
			}, {
				"name" : "hiveserver2_spark_yarn_driver_memory_overhead",
				"value" : "102"
			}, {
				"name" : "hiveserver2_spark_yarn_executor_memory_overhead",
				"value" : "153"
			} ]
			} ],
			"items" : [ {
			"name" : "hive_metastore_database_host",
			"value" : "ip-172-31-1-96.us-west-1.compute.internal"
			}, {
			"name" : "hive_metastore_database_name",
			"value" : "hive"
			}, {
			"name" : "hive_metastore_database_password",
			"value" : "123456"
			}, {
			"name" : "mapreduce_yarn_service",
			"value" : "yarn"
			}, {
			"name" : "zookeeper_service",
			"value" : "zookeeper"
			} ]
		},
		"roles" : [ {
			"name" : "hive-GATEWAY-2d0a9371a899499d432e52671b7d65b3",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hive-GATEWAY-6816accef44d80e81118421075bf2b43",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hive-GATEWAY-6cb52a1519f8187c1df01496c43d6fe8",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hive-GATEWAY-8751d14a1b7d9196973d9d73c923f3ac",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hive-GATEWAY-b3f39c9653941ed458a323dc32878b29",
			"type" : "GATEWAY",
			"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
			},
			"config" : {
			"items" : [ ]
			}
		}, {
			"name" : "hive-HIVEMETASTORE-2d0a9371a899499d432e52671b7d65b3",
			"type" : "HIVEMETASTORE",
			"hostRef" : {
			"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "3977gtaneztuerc8gz5rfiboo"
			} ]
			}
		}, {
			"name" : "hive-HIVESERVER2-2d0a9371a899499d432e52671b7d65b3",
			"type" : "HIVESERVER2",
			"hostRef" : {
			"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "cs8zlzsi62ctfd557d6x6ak58"
			} ]
			}
		} ],
		"displayName" : "Hive"
		}, {
		"name" : "oozie",
		"type" : "OOZIE",
		"config" : {
			"roleTypeConfigs" : [ {
			"roleType" : "OOZIE_SERVER",
			"items" : [ {
				"name" : "oozie_database_host",
				"value" : "ip-172-31-1-96.us-west-1.compute.internal"
			}, {
				"name" : "oozie_database_password",
				"value" : "123456"
			}, {
				"name" : "oozie_database_type",
				"value" : "mysql"
			}, {
				"name" : "oozie_database_user",
				"value" : "oozie"
			}, {
				"name" : "oozie_java_heapsize",
				"value" : "52428800"
			} ]
			} ],
			"items" : [ {
			"name" : "hive_service",
			"value" : "hive"
			}, {
			"name" : "mapreduce_yarn_service",
			"value" : "yarn"
			}, {
			"name" : "zookeeper_service",
			"value" : "zookeeper"
			} ]
		},
		"roles" : [ {
			"name" : "oozie-OOZIE_SERVER-6816accef44d80e81118421075bf2b43",
			"type" : "OOZIE_SERVER",
			"hostRef" : {
			"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "dkzzvv2b4yhm32m29p1iaq1wy"
			} ]
			}
		} ],
		"displayName" : "Oozie"
		}, {
		"name" : "hue",
		"type" : "HUE",
		"config" : {
			"roleTypeConfigs" : [ ],
			"items" : [ {
			"name" : "database_host",
			"value" : "ip-172-31-1-96.us-west-1.compute.internal"
			}, {
			"name" : "database_password",
			"value" : "123456"
			}, {
			"name" : "database_type",
			"value" : "mysql"
			}, {
			"name" : "hive_service",
			"value" : "hive"
			}, {
			"name" : "hue_webhdfs",
			"value" : "hdfs-HTTPFS-6cb52a1519f8187c1df01496c43d6fe8"
			}, {
			"name" : "oozie_service",
			"value" : "oozie"
			}, {
			"name" : "zookeeper_service",
			"value" : "zookeeper"
			} ]
		},
		"roles" : [ {
			"name" : "hue-HUE_SERVER-b3f39c9653941ed458a323dc32878b29",
			"type" : "HUE_SERVER",
			"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
			},
			"config" : {
			"items" : [ {
				"name" : "role_jceks_password",
				"value" : "a5mnpho2wwsusux68w7v0bk5t"
			}, {
				"name" : "secret_key",
				"value" : "qoSQjDEaT2U5YxrzJWRj7T6oBgaSJf"
			} ]
			}
		} ],
		"displayName" : "Hue"
		} ]
	} ],
	"hosts" : [ {
		"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b",
		"ipAddress" : "172.31.1.58",
		"hostname" : "ip-172-31-1-58.us-west-1.compute.internal",
		"rackId" : "/default",
		"config" : {
		"items" : [ ]
		}
	}, {
		"hostId" : "965cd56c-1058-4667-83db-af175c2dfff3",
		"ipAddress" : "172.31.1.96",
		"hostname" : "ip-172-31-1-96.us-west-1.compute.internal",
		"rackId" : "/default",
		"config" : {
		"items" : [ ]
		}
	}, {
		"hostId" : "a1c9d40c-2165-49a2-830a-7afd8debea77",
		"ipAddress" : "172.31.13.171",
		"hostname" : "ip-172-31-13-171.us-west-1.compute.internal",
		"rackId" : "/default",
		"config" : {
		"items" : [ ]
		}
	}, {
		"hostId" : "81dc5e0d-8eb1-4e3c-99a4-a09f1fbd3f01",
		"ipAddress" : "172.31.15.67",
		"hostname" : "ip-172-31-15-67.us-west-1.compute.internal",
		"rackId" : "/default",
		"config" : {
		"items" : [ ]
		}
	}, {
		"hostId" : "b8ce52bc-8eef-410e-84d5-29064c200fa4",
		"ipAddress" : "172.31.5.179",
		"hostname" : "ip-172-31-5-179.us-west-1.compute.internal",
		"rackId" : "/default",
		"config" : {
		"items" : [ ]
		}
	} ],
	"users" : [ {
		"name" : "__cloudera_internal_user__mgmt-EVENTSERVER-b3f39c9653941ed458a323dc32878b29",
		"roles" : [ "ROLE_USER" ],
		"pwHash" : "a972f778d74855f0eb68b6b67d07caf6d4ff7e0ee4d8209906ec5bdae0768961",
		"pwSalt" : -456376753999078081,
		"pwLogin" : true
	}, {
		"name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-b3f39c9653941ed458a323dc32878b29",
		"roles" : [ "ROLE_USER" ],
		"pwHash" : "aca60d0fc2b1f301766e89963b725d98b7b587e86eaaebf0f789ee45fab5dd6b",
		"pwSalt" : 8797420454978598485,
		"pwLogin" : true
	}, {
		"name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-b3f39c9653941ed458a323dc32878b29",
		"roles" : [ "ROLE_USER" ],
		"pwHash" : "f6a4d3aea62b3ef3a33aea0d8dbead7822321dfafe24bbeb80f6e9d1deb5e377",
		"pwSalt" : 8271123156641292560,
		"pwLogin" : true
	}, {
		"name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-b3f39c9653941ed458a323dc32878b29",
		"roles" : [ "ROLE_USER" ],
		"pwHash" : "800417989c8b0f0c208b69072bef51c63b89faf8118f7001fd4e28257eb0ddcc",
		"pwSalt" : -566136412407402255,
		"pwLogin" : true
	}, {
		"name" : "admin",
		"roles" : [ "ROLE_LIMITED" ],
		"pwHash" : "1c9fb1fdbd5739f1428217d16ef6240a0904d820f56ea3724979102587ea39dc",
		"pwSalt" : 1221312545100934446,
		"pwLogin" : true
	}, {
		"name" : "minotaur",
		"roles" : [ "ROLE_CONFIGURATOR" ],
		"pwHash" : "b4b81030efd1279d05a5a031d05f68fd7e6971f3aeb644ea23791befac74fab1",
		"pwSalt" : 3277900362795248565,
		"pwLogin" : true
	}, {
		"name" : "wk109353794",
		"roles" : [ "ROLE_ADMIN" ],
		"pwHash" : "7fcfe73e1cf9d355e4954016bea4cb102d663e0b117930faf52951d694d57f72",
		"pwSalt" : -4252500012948008886,
		"pwLogin" : true
	} ],
	"versionInfo" : {
		"version" : "5.9.2",
		"buildUser" : "jenkins",
		"buildTimestamp" : "20170330-1814",
		"gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
		"snapshot" : false
	},
	"managementService" : {
		"name" : "mgmt",
		"type" : "MGMT",
		"config" : {
		"roleTypeConfigs" : [ {
			"roleType" : "EVENTSERVER",
			"items" : [ {
			"name" : "event_server_heapsize",
			"value" : "839909376"
			} ]
		}, {
			"roleType" : "HOSTMONITOR",
			"items" : [ {
			"name" : "firehose_heapsize",
			"value" : "839909376"
			}, {
			"name" : "firehose_non_java_memory_bytes",
			"value" : "1091567616"
			} ]
		}, {
			"roleType" : "REPORTSMANAGER",
			"items" : [ {
			"name" : "headlamp_database_host",
			"value" : "ip-172-31-1-96.us-west-1.compute.internal"
			}, {
			"name" : "headlamp_database_name",
			"value" : "report"
			}, {
			"name" : "headlamp_database_password",
			"value" : "123456"
			}, {
			"name" : "headlamp_database_user",
			"value" : "report"
			}, {
			"name" : "headlamp_heapsize",
			"value" : "839909376"
			} ]
		}, {
			"roleType" : "SERVICEMONITOR",
			"items" : [ {
			"name" : "firehose_heapsize",
			"value" : "839909376"
			}, {
			"name" : "firehose_non_java_memory_bytes",
			"value" : "1091567616"
			} ]
		} ],
		"items" : [ ]
		},
		"roles" : [ {
		"name" : "mgmt-ALERTPUBLISHER-b3f39c9653941ed458a323dc32878b29",
		"type" : "ALERTPUBLISHER",
		"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
		},
		"config" : {
			"items" : [ {
			"name" : "role_jceks_password",
			"value" : "a40ai2z97y65r5kaz80tttf0j"
			} ]
		}
		}, {
		"name" : "mgmt-EVENTSERVER-b3f39c9653941ed458a323dc32878b29",
		"type" : "EVENTSERVER",
		"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
		},
		"config" : {
			"items" : [ {
			"name" : "role_jceks_password",
			"value" : "lb79hz6gnrls1vxff6gobfbj"
			} ]
		}
		}, {
		"name" : "mgmt-HOSTMONITOR-b3f39c9653941ed458a323dc32878b29",
		"type" : "HOSTMONITOR",
		"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
		},
		"config" : {
			"items" : [ {
			"name" : "role_jceks_password",
			"value" : "7u7tp5i1u06l2abyho60663z2"
			} ]
		}
		}, {
		"name" : "mgmt-REPORTSMANAGER-b3f39c9653941ed458a323dc32878b29",
		"type" : "REPORTSMANAGER",
		"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
		},
		"config" : {
			"items" : [ {
			"name" : "role_jceks_password",
			"value" : "yev3holfk8o11dxfdk46mlh4"
			} ]
		}
		}, {
		"name" : "mgmt-SERVICEMONITOR-b3f39c9653941ed458a323dc32878b29",
		"type" : "SERVICEMONITOR",
		"hostRef" : {
			"hostId" : "98f67d9a-4dfc-4b4b-8e8a-333b40dc997b"
		},
		"config" : {
			"items" : [ {
			"name" : "role_jceks_password",
			"value" : "2casugln0d6qrbqkraxo65zsb"
			} ]
		}
		} ],
		"displayName" : "Cloudera Management Service"
	},
	"managerSettings" : {
		"items" : [ {
		"name" : "CLUSTER_STATS_START",
		"value" : "10/27/2012 8:50"
		}, {
		"name" : "PUBLIC_CLOUD_STATUS",
		"value" : "ON_PUBLIC_CLOUD"
		}, {
		"name" : "REMOTE_PARCEL_REPO_URLS",
		"value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,http://ec2-52-53-162-208.us-west-1.compute.amazonaws.com/cdh5.11/cdh/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
		} ]
	}
	}