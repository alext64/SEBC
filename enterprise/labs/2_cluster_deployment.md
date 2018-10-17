```json
{
  "timestamp" : "2018-10-17T08:57:39.640Z",
  "clusters" : [ {
    "name" : "alext64",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-9e10778d57441ff766fef456596e75b6",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "50qu1a95kxreoy6uiv2ai1u8j"
          }, {
            "name" : "serverId",
            "value" : "5"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-e616787afd688759b5b5a088f27ab248",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bs90xu7ywteyr0pk0ta2761m5"
          }, {
            "name" : "serverId",
            "value" : "4"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8txx9q0l6ysnqp9y51p0q17rx"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "sebc01"
          }, {
            "name" : "oozie_database_password",
            "value" : "Amon_amon1"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "738197504"
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
        "name" : "oozie-OOZIE_SERVER-9e10778d57441ff766fef456596e75b6",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bqvleetp3fn5pbsi5gl9ohc91"
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
          "value" : "sebc01"
        }, {
          "name" : "database_password",
          "value" : "Amon_amon1"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-f3c0b57a82de4882b19615f2765e78cf"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-9e10778d57441ff766fef456596e75b6",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "36xcny8w3xiggy3uarivalskt"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-9e10778d57441ff766fef456596e75b6",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "9c94312d-8461-4c8d-ac05-b4f317dabde0"
          }, {
            "name" : "role_jceks_password",
            "value" : "47tfpasjk61mnpqvu3sqnv0ax"
          }, {
            "name" : "secret_key",
            "value" : "gI4vxuTBgqv7jZHb6OXBqmooKXrros"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "738197504"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data/1/dfs/dn,/data/2/dfs/dn,/data/3/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "8441526681"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
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
            "value" : "/data/1/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/data/1/dfs/nn,/data/2/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "738197504"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data/1/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "738197504"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_client_use_datanode_hostname",
          "value" : "true"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "rqk4dTWh2CwuliYy83y2dZlIjHZH7p"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "yIbE4eSGFyxAlIgSMsgmTXMTgu32be"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "mKdzgB0H2oFPIbYUaYC05M6L6hw41Z"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-9e10778d57441ff766fef456596e75b6",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-364a76fca2cf4518353e9d759b52a9ce",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "b60836cf-3bb0-4909-aaba-529a678ba3b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ufr9e7d0qtqjqxb7mcvlxlwq"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-51e24c456cfdd8b69f2fc4f164833b90",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "1d27b3fe-24a9-4462-9d96-e98cb7178716"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6bwg7h0kpbtugxvr3gvm47w39"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7o0pezrwrty7s1zxs2jb0hieo"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-9e10778d57441ff766fef456596e75b6",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2uj2rb8bhvb5yzjsfum3egb0x"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-e616787afd688759b5b5a088f27ab248",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2920k35m90lq8m31g8re0g9fk"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7y71iv2fos3wui7uk2w6nuysf"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-9e10778d57441ff766fef456596e75b6",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1cc2vt5dhrvl3oes028lzjav7"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-e616787afd688759b5b5a088f27ab248",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "41ebqg8vzaamkdag300lac0lz"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1rot8mhkz2dwey3bfb1yayflj"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-9e10778d57441ff766fef456596e75b6",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
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
            "value" : "45"
          }, {
            "name" : "role_jceks_password",
            "value" : "diq6aocteb1juffm4qpdmmeae"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-e616787afd688759b5b5a088f27ab248",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
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
            "value" : "4hflj7a19s9fdm615f7397asn"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "10"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "738197504"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/data/1/yarn/nm,/data/2/yarn/nm,/data/3/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data/1/yarn/container-logs,/data/2/yarn/container-logs,/data/3/yarn/container-logs,/data/4/yarn/container-logs,/data/5/yarn/container-logs,/mnt/resource/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "7"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3660"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "738197504"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5989"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "7"
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
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "hVsHPEtYtT5OrT8uAHC8SrPPw45JHz"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-e616787afd688759b5b5a088f27ab248",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-9e10778d57441ff766fef456596e75b6",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d1qvahhkxmhxxmydbmlqg9pt4"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-364a76fca2cf4518353e9d759b52a9ce",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "b60836cf-3bb0-4909-aaba-529a678ba3b8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1ledwf8zrnne9ohmfb31gvqcz"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-51e24c456cfdd8b69f2fc4f164833b90",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "1d27b3fe-24a9-4462-9d96-e98cb7178716"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "911qihvl7hm0d8tkuwy5sfy8z"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c73hola9h4n3qc39iq1bmttiz"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-9e10778d57441ff766fef456596e75b6",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "51"
          }, {
            "name" : "role_jceks_password",
            "value" : "9ds6gcw5xv769eyc3e1apfr3"
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
            "value" : "738197504"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "738197504"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2075813478"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "349"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "sebc01"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "Amon_amon1"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-364a76fca2cf4518353e9d759b52a9ce",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b60836cf-3bb0-4909-aaba-529a678ba3b8"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-51e24c456cfdd8b69f2fc4f164833b90",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1d27b3fe-24a9-4462-9d96-e98cb7178716"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9e10778d57441ff766fef456596e75b6",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-e616787afd688759b5b5a088f27ab248",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f3c0b57a82de4882b19615f2765e78cf",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-9e10778d57441ff766fef456596e75b6",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4e0a6wwnq23n7li6wra8exrb6"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-9e10778d57441ff766fef456596e75b6",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4yhtsfklcxmc8poc2gv3vuf22"
          } ]
        }
      } ],
      "displayName" : "Hive"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763",
    "ipAddress" : "10.0.0.9",
    "hostname" : "sebc01",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "05d69656-6dfd-4da7-9001-82af6ddeebcf",
    "ipAddress" : "10.0.0.10",
    "hostname" : "sebc02",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "c624ff6a-5833-448e-8da8-7b488f26071a",
    "ipAddress" : "10.0.0.11",
    "hostname" : "sebc03",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "b60836cf-3bb0-4909-aaba-529a678ba3b8",
    "ipAddress" : "10.0.0.12",
    "hostname" : "sebc04",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "1d27b3fe-24a9-4462-9d96-e98cb7178716",
    "ipAddress" : "10.0.0.13",
    "hostname" : "sebc05",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__d136f0d3-5c2f-4866-8abc-7361f99df823",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "94fd70ec125a9eff58ac01ef785f7bf36639977d60631597d88af91e56e4a33f",
    "pwSalt" : 6590452553464940233,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__eb69769f-702b-4272-9853-cb1d776b5247",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e570af3f881718663e1a7bf46d7bace8ba48b52dcbc9e54a63315653531e1d5b",
    "pwSalt" : -6626681744950536254,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-9e10778d57441ff766fef456596e75b6",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "4a7ecdcd6042913c9f90afef1e85c5242b75ca784140b9626dbf735da9cd9696",
    "pwSalt" : -4871857292159016850,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-9e10778d57441ff766fef456596e75b6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0cdd192e33e90fd6d59bf7d6aefdc11f3e7ff825515905b580d5bf820915e0f7",
    "pwSalt" : -8515536204705128098,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-9e10778d57441ff766fef456596e75b6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d0d02c304e9d1a3110c3fd972a486573b606a952cfc4b48e56581c8e40d848f9",
    "pwSalt" : -3444713157719299782,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-9e10778d57441ff766fef456596e75b6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "babb6e773965c2e9033ae5b74d1ab6f6f5b4cca149baa7aa1e80269f6471a216",
    "pwSalt" : -6724491591668705014,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-9e10778d57441ff766fef456596e75b6",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "877867ee6ddc3c6137835da25f207596c857a3d9309b57a00e321b08c28968f1",
    "pwSalt" : -177149035303533870,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "9914eb6800a2f391ad4373fda571713ab02e48b44d537bdd7edf0adc6122980f",
    "pwSalt" : 2559382172300613290,
    "pwLogin" : true
  }, {
    "name" : "alext64",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "cc26b6f8fa579e3b1d2e3d766941c76292034ec608a93e4d11d4f522c8ef82a5",
    "pwSalt" : 5312079614113714423,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "61935f2de30ddd9483a2c0b7b3ac5306db6c5bd3f4e7c1f8a0f0ebebfd0fbe26",
    "pwSalt" : 6893384035246267052,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.13.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20180328-1830",
    "gitHash" : "f90c58536c252d70a23bde6d94514d92a1f111d4",
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
          "value" : "738197504"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "738197504"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "959447040"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "sebc01"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "Amon_amon1"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "738197504"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "738197504"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "959447040"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-9e10778d57441ff766fef456596e75b6",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7k0qdg75z7errbbg28wfa5ilp"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-9e10778d57441ff766fef456596e75b6",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "9e3hctefasjtmhuoyjsa9afjn"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-9e10778d57441ff766fef456596e75b6",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "b0ritli067rpe193a4xkdgvt9"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-9e10778d57441ff766fef456596e75b6",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "75txnxxzgxtjbvs0d39h4sbcn"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-9e10778d57441ff766fef456596e75b6",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "af82cdff-30d4-40bf-95b1-32171d95a763"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "39zhc60trdmfbxdreue7fpwqb"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 3:10"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://sebc02.westeurope.cloudapp.azure.com/cloudera-repos/cdh5/parcels/5.14.4/,http://sebc02.westeurope.cloudapp.azure.com/cloudera-repos/accumulo-c5/parcels/1.7.2/"
    }, {
      "name" : "SESSION_TIMEOUT",
      "value" : "28800"
    } ]
  }
}
```

