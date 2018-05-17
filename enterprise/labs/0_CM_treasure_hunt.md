1. What is uber optimization?

When a MapReduce job is submitted, ResourceManager launches the ApplicationMaster process (For MapReduce the ApplicationMaster is MRAppMaster) on a container. Then ApplicationMaster retrieves the number of input splits for the job and based on that it decides the number of mappers that has to be launched and also the number of reducers that has to be launched as per the configuration.

At this juncture ApplicationMaster has to decide whether to negotiate resources with the ResourceManager’s scheduler to run the map and reduce tasks or run the job sequentially with in the same JVM where ApplicationMaster is running.

This decision making by ApplicationMaster happens only if Uber mode is set to true in Hadoop. If uber mode is true and ApplicationMaster decides to run the MapReduce job with in the same JVM then the job is said to be running as uber task in YARN.

While running a MapReduce job in Hadoop2 you might have noticed this message on the console-

Job job_XXXXX_xxxx running in uber mode : false
This message will be displayed if you have not modified the default which is false for uber mode in Hadoop.
Why to run job as uber task in YARN

For running a job as uber task in YARN, job has to be "sufficiently small".

If a job is small enough, the ApplicationMaster can decide that the process of negotiating with ResourceManager to get resource containers, contacting the node managers of remote nodes and running tasks on those containers requires more effort than running the job sequentially on the same JVM as ApplicationMaster. Then it can run the job as uber task in YARN.

There are certain configuration parameters that help ApplicationMaster to decide when the job is small enough to be run as uber task in YARN. By default the values are; there should be less than 10 mappers, only one reducer and maximum input bytes should not be more than a HDFS block size.

Uber mode configuration parameters in Hadoop

Configurations parameters required for uber mode are set in etc/hadoop/mapred-site.xml

mapreduce.job.ubertask.enable - Used to set the uber mode as true or false. Set to true means small-jobs "ubertask" optimization is enabled. Default value is false.
mapreduce.job.ubertask.maxmaps - This configuration sets the maximum number of maps, beyond which job is considered too big for the ubertasking optimization. Users may override this value, but only downward. Default value is 9.
mapreduce.job.ubertask.maxreduces - This configuration sets the maximum number of reduces, beyond which job is considered too big for the ubertasking optimization. Currently support is for one reduce only. Larger values will be ignored. Users may override this value, but only downward. Default value is 1.
mapreduce.job.ubertask.maxbytes- Threshold for number of input bytes, beyond which job is considered too big for the ubertasking optimization. If no value is specified, dfs.block.size is used as a default. In case of HDFS it would mean HDFS bock size. Users may override this value, but only downward.

2. Where in CM is the Kerberos Security Realm value displayed?

Sol: Path Clouderamanager Home Page -> Administration -> settings -> security (select security in category).

3.Which CDH service(s) host a property for enabling Kerberos authentication?
	
sol:

4.How do you upgrade the CM agents?

sol:

5. Give the tsquery statement used to chart Hue's CPU utilization?

sol: select cpu_user_rate where roleType=HUE_SERVER

6.Name all the roles that make up the Hive service

sol: Hive service is composed of  below services:
     1. Hivemetastore
     2. hive server2
     3. webhcatalog service

7. What steps must be completed before integrating Cloudera Manager with Kerberos?

  1. Java Criptography extension (JCE ) needs to be installed on all the hosts

  2. Install MIT Kerberos 

  