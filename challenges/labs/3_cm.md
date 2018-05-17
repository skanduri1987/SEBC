
[hdfs@instance-2 ~]$ hdfs dfs -mkdir /user/jimenez
[hdfs@instance-2 ~]$ hdfs dfs -mkdir /user/beltran
[hdfs@instance-2 ~]$ hdfs dfs -ls /user
Found 6 items
drwxr-xr-x   - hdfs   supergroup          0 2018-05-17 08:31 /user/beltran
drwxrwxrwx   - mapred hadoop              0 2018-05-17 08:22 /user/history
drwxrwxr-t   - hive   hive                0 2018-05-17 08:23 /user/hive
drwxrwxr-x   - hue    hue                 0 2018-05-17 08:24 /user/hue
drwxr-xr-x   - hdfs   supergroup          0 2018-05-17 08:31 /user/jimenez
drwxrwxr-x   - oozie  oozie               0 2018-05-17 08:24 /user/oozie


[hdfs@instance-2 ~]$ curl -u admin:admin 'http://localhost:7180/api/v11/clusters/skanduri1987/services'
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/zookeeper/instances",
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
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/oozie",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/oozie/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hue",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hue/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HUE_LOAD_BALANCER_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hdfs/instances",
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
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/yarn",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/yarn/instances",
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
      "summary" : "DISABLED",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hbase",
    "type" : "HBASE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hbase",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hbase/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HBASE_MASTER_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HBASE_REGION_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HBase",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/serviceRedirect/hive/instances",
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
}[hdfs@instance-2 ~]$ 


[hdfs@instance-2 ~]$ curl -u admin:admin http://localhost:7180/api/v11/hosts
{
  "items" : [ {
    "hostId" : "0d4570c1-0320-4514-8bd5-97441c597f4a",
    "ipAddress" : "10.142.0.2",
    "hostname" : "instance-1.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/0d4570c1-0320-4514-8bd5-97441c597f4a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "575daf1f-ebc3-4131-b5db-82b94071870f",
    "ipAddress" : "10.142.0.3",
    "hostname" : "instance-2.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/575daf1f-ebc3-4131-b5db-82b94071870f",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "d16e153d-f275-4c01-bfe4-92a74486e316",
    "ipAddress" : "10.128.0.2",
    "hostname" : "instance-3.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/d16e153d-f275-4c01-bfe4-92a74486e316",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600504832
  }, {
    "hostId" : "eec89797-2118-4584-9781-99993fa4359a",
    "ipAddress" : "10.128.0.3",
    "hostname" : "instance-4.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/eec89797-2118-4584-9781-99993fa4359a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600513024
  }, {
    "hostId" : "45163869-68eb-49b0-af2e-6b5e8525193c",
    "ipAddress" : "10.138.0.2",
    "hostname" : "instance-5.c.trusty-axe-170408.internal",
    "rackId" : "/default",
    "hostUrl" : "http://instance-2.c.trusty-axe-170408.internal:7180/cmf/hostRedirect/45163869-68eb-49b0-af2e-6b5e8525193c",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15600513024
  } ]
}[hdfs@instance-2 ~]$ 
