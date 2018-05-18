[root@instance-1 cdh512]# curl -u admin:admin "http://localhost:7180/api/v5/hosts"
{
  "items" : [ {
    "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7",
    "ipAddress" : "10.142.0.2",
    "hostname" : "instance-1.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/ca4026a2-9701-4464-a42e-a9d4c5cd6cb7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338",
    "ipAddress" : "10.128.0.2",
    "hostname" : "instance-2.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/e40a6027-34a4-4e9c-9324-785a3c3a3338",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67",
    "ipAddress" : "10.128.0.3",
    "hostname" : "instance-3.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/57390e99-d2c7-4497-a512-c978e9470c67",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "807cc14d-001e-4cd9-b122-0f0a52518e54",
    "ipAddress" : "10.142.0.3",
    "hostname" : "instance-4.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/807cc14d-001e-4cd9-b122-0f0a52518e54",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "229ae65e-db79-45b0-a13c-a4f822c5d859",
    "ipAddress" : "10.138.0.2",
    "hostname" : "instance-5.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/229ae65e-db79-45b0-a13c-a4f822c5d859",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "totalPhysMemBytes" : 15600513024
  } ]
}[root@instance-1 cdh512]# curl -u admin:admin 'http://internalIP:7180/api/v11/clusters/skanduri1987/services"
> ^C
[root@instance-1 cdh512]# curl -u admin:admin "http://internalIP:7180/api/v11/clusters/skanduri1987/services"
curl: (6) Could not resolve host: internalIP; Name or service not known
[root@instance-1 cdh512]# curl -u admin:admin "http://localhost:7180/api/v11/clusters/skanduri1987/services"
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/zookeeper/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hdfs/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FAILOVER_CONTROLLERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/yarn",
    "roleInstancesUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/yarn/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl" : "http://instance-1.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hive/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HIVE_WEBHCATS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive",
    "entityStatus" : "GOOD_HEALTH"
  } ]
}[root@instance-1 cdh512]# curl -u admin:admin "http://localhost:7180/api/v12/cm/deployment">deployment.json
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 37410    0 37410    0     0   194k      0 --:--:-- --:--:-- --:--:--  195k
[root@instance-1 cdh512]# ll
total 40
drwxr-xr-x 3 root root    18 May 18 04:32 cloudera-cdh5
-rw-r--r-- 1 root root 37410 May 18 04:58 deployment.json
[root@instance-1 cdh512]# cat deployment.json 
{
  "timestamp" : "2018-05-18T04:58:45.569Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "skanduri1987",
    "version" : "CDH5",
    "fullVersion" : "5.11.2",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "efyihscwxefljgm3jsw05wu1t"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-c48857edf57032b593862cbb93881077",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ef73uv4dpuvyvsmki16we1gj"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e6l03bhhda1z2c5tq5i7l6g5a"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "V16iEy5pDB4TOefqLuDZGhERsSZCfP"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "qFvSkRXwtfseXQ62TbFw1Bdy5REMAt"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "Mzjn9Zc8THI0gKwTOV4kj9pyCDwAAY"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-249daa78a40930349c95a2318a1c4241",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "229ae65e-db79-45b0-a13c-a4f822c5d859"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c49kdi67r5x0ghd00u9pn07p1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-2f169d084aa1ccc5a51874b6d8545b83",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "807cc14d-001e-4cd9-b122-0f0a52518e54"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "462jxxvzza3j0pylt53vyabm0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9striomoknofjzpkg0ksnkn62"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9waxzmvmswxlsnjlvclko9r6c"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c48857edf57032b593862cbb93881077",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "14g74wr5zb6idwj3k9c9rdz14"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-c48857edf57032b593862cbb93881077",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e2n1gtihjti1zihsni638k9to"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4qhsfbxt96p74a4sz0hifekrj"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c48857edf57032b593862cbb93881077",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "40t6xp4vwbddmiu279u5tz424"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7hg43f04z4vrm6vw2mkmflhy6"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
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
            "value" : "31"
          }, {
            "name" : "role_jceks_password",
            "value" : "gnto9z41h68hy3mtuk2mcwdi"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-c48857edf57032b593862cbb93881077",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
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
            "value" : "33"
          }, {
            "name" : "role_jceks_password",
            "value" : "6os3d9suauq5ycc5wiqkkrt8z"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_nfsgateway_scm_health",
            "value" : "true"
          }, {
            "name" : "role_jceks_password",
            "value" : "cbbjr812fujk8z4mdbiku4a38"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NFSGATEWAY-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "742391808"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367486464"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "742391808"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "742391808"
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "cm_yarn_container_usage_job_user",
          "value" : "santosh"
        }, {
          "name" : "cm_yarn_enable_container_usage_aggregation",
          "value" : "true"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "ScBPSAXjrKMKWLVAizKd7VafpcoYId"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8eac9oq9k23bwput9shrplrcq"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-249daa78a40930349c95a2318a1c4241",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "229ae65e-db79-45b0-a13c-a4f822c5d859"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5kzzxqhoadtein6gj3mpn52zx"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-2f169d084aa1ccc5a51874b6d8545b83",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "807cc14d-001e-4cd9-b122-0f0a52518e54"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c33pifv6er3r2heoewiplojdc"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bcclutu2j5uxsiacj1335m9l1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "48"
          }, {
            "name" : "role_jceks_password",
            "value" : "5w8iyf5y3966ll178y9it01ht"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "52428800"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
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
            "value" : "2814"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
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
            "value" : "5143"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "52428800"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5143"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        }
      } ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "instance-1.c.trusty-axe-170408.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "bigdata"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-249daa78a40930349c95a2318a1c4241",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "229ae65e-db79-45b0-a13c-a4f822c5d859"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-2f169d084aa1ccc5a51874b6d8545b83",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "807cc14d-001e-4cd9-b122-0f0a52518e54"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-c48857edf57032b593862cbb93881077",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-de3d0936e5cc79677c4504e654dddf9a",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "47df8jt0cyl5tipyv6sy0u0l8"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-c48857edf57032b593862cbb93881077",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dkgref0oh4oh6d3uumkwk6au1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-WEBHCAT-c48857edf57032b593862cbb93881077",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "6x2lCqRIh9Fb2GP7aM9ChFaRC5JLnj"
          }, {
            "name" : "role_jceks_password",
            "value" : "6trfkimv0zsiw32prbl6mydy0"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-WEBHCAT-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "52428800"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2508088934"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "422"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
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
        "name" : "oozie-OOZIE_SERVER-3af70c4339b3c0e2697d168f4c5e7cfe",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "agz5mjzboxjgv2q8tau49oknp"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "instance-1.c.trusty-axe-170408.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "bigdata"
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
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7",
    "ipAddress" : "10.142.0.2",
    "hostname" : "instance-1.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "e40a6027-34a4-4e9c-9324-785a3c3a3338",
    "ipAddress" : "10.128.0.2",
    "hostname" : "instance-2.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "57390e99-d2c7-4497-a512-c978e9470c67",
    "ipAddress" : "10.128.0.3",
    "hostname" : "instance-3.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "807cc14d-001e-4cd9-b122-0f0a52518e54",
    "ipAddress" : "10.142.0.3",
    "hostname" : "instance-4.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "229ae65e-db79-45b0-a13c-a4f822c5d859",
    "ipAddress" : "10.138.0.2",
    "hostname" : "instance-5.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-3af70c4339b3c0e2697d168f4c5e7cfe",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "aaa59ae95e9d1c105ff2d5d89125d662a874f29a1b459cfe84146230c25bb045",
    "pwSalt" : 911967047667434029,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-3af70c4339b3c0e2697d168f4c5e7cfe",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6d2d48874dcbd226d621c1baceca75264263e2d0d9e90d2a607249cbd9f2d6c1",
    "pwSalt" : -3525903241948893759,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-3af70c4339b3c0e2697d168f4c5e7cfe",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2e714c70965f41a75532c6414c57b3db43d354cade5d5114148d985afe19fb78",
    "pwSalt" : -7341394149345917300,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-3af70c4339b3c0e2697d168f4c5e7cfe",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5aab11b96ed88830b302d6c2e1cead061b2e4586f567c08cb307d6c2671a08a7",
    "pwSalt" : -577927149824865744,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "6845b1c55dc1aa667234fc969a9ef5470ca749c8ee22f420ec6b8dd7ac592905",
    "pwSalt" : -535966332733978064,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-3af70c4339b3c0e2697d168f4c5e7cfe",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "1nc9jgurjd5ez3ggx2m3i538e"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-3af70c4339b3c0e2697d168f4c5e7cfe",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7xc1yt0s4ka2di1t9v24vcui6"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-3af70c4339b3c0e2697d168f4c5e7cfe",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eyepu8n285ocuqp4rqlf9vnxn"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-3af70c4339b3c0e2697d168f4c5e7cfe",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "yckyge5hnfyw4lpl9dstkvhl"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-3af70c4339b3c0e2697d168f4c5e7cfe",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "ca4026a2-9701-4464-a42e-a9d4c5cd6cb7"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7v0d73qw31wav4k7g0ra91bz6"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "instance-1.c.trusty-axe-170408.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "bigdata"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "displayName" : "Telemetry Publisher Default Group",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/24/2012 14:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,htt
ps://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.co
m/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/l
atest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  },
  "allHostsConfig" : {
    "items" : [ ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
}[root@instance-1 cdh512]# hdfs dfs -ls /
Found 2 items
drwxrwxrwt   - hdfs supergroup          0 2018-05-18 04:55 /tmp
drwxr-xr-x   - hdfs supergroup          0 2018-05-18 04:57 /user
[root@instance-1 cdh512]# su - hdsf
su: user hdsf does not exist
[root@instance-1 cdh512]# su - hdfs
[hdfs@instance-1 ~]$ hdfs dfs -mkdir /user/thanos
[hdfs@instance-1 ~]$ hdfs dfs -mkdir /user/hulk
[hdfs@instance-1 ~]$ hdfs dfs -mkdir /usergroot
[hdfs@instance-1 ~]$ hdfs dfs -mkdir /user/groot
[hdfs@instance-1 ~]$ hdfs dfs -ls /user
Found 8 items
drwxr-xr-x   - hdfs    supergroup          0 2018-05-18 05:00 /user/groot
drwxrwxrwx   - mapred  hadoop              0 2018-05-18 04:52 /user/history
drwxrwxr-t   - hive    hive                0 2018-05-18 04:55 /user/hive
drwxrwxr-x   - hue     hue                 0 2018-05-18 04:55 /user/hue
drwxr-xr-x   - hdfs    supergroup          0 2018-05-18 05:00 /user/hulk
drwxrwxr-x   - oozie   oozie               0 2018-05-18 04:57 /user/oozie
drwxr-xr-x   - santosh santosh             0 2018-05-18 04:53 /user/santosh
drwxr-xr-x   - hdfs    supergroup          0 2018-05-18 05:00 /user/thanos