[jimenez@instance-1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen  -Dmapred.map.tasks=8  -Ddfs.block.size=67108864 65536000 /user/j
imenez/tgen
18/05/17 09:00:07 INFO client.RMProxy: Connecting to ResourceManager at instance-1.c.trusty-axe-170408.internal/10.142.0.2:8032
18/05/17 09:00:08 INFO terasort.TeraGen: Generating 65536000 using 8
18/05/17 09:00:09 INFO mapreduce.JobSubmitter: number of splits:8
18/05/17 09:00:09 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/17 09:00:09 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/17 09:00:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526545375216_0001
18/05/17 09:00:11 INFO impl.YarnClientImpl: Submitted application application_1526545375216_0001
18/05/17 09:00:11 INFO mapreduce.Job: The url to track the job: http://instance-1.c.trusty-axe-170408.internal:8088/proxy/application_1526545375216_0001/
18/05/17 09:00:11 INFO mapreduce.Job: Running job: job_1526545375216_0001
18/05/17 09:00:19 INFO mapreduce.Job: Job job_1526545375216_0001 running in uber mode : false
18/05/17 09:08:30 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1184256
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=682
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters 
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=1900667
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=1900667
                Total vcore-milliseconds taken by all map tasks=1900667
                Total megabyte-milliseconds taken by all map tasks=1946283008
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=682
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1209
                CPU time spent (ms)=123640
                Physical memory (bytes) snapshot=2673528832
                Virtual memory (bytes) snapshot=22416392192
                Total committed heap usage (bytes)=2200436736
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=6553600000
real    8m24.824s
user    0m9.848s
sys     0m0.883s

[jimenez@instance-1 ~]$ hdfs dfs -ls /user/jimenez/tgen
Found 9 items
-rw-r--r--   3 jimenez supergroup          0 2018-05-17 09:08 /user/jimenez/tgen/_SUCCESS
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:04 /user/jimenez/tgen/part-m-00000
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:04 /user/jimenez/tgen/part-m-00001
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:04 /user/jimenez/tgen/part-m-00002
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:04 /user/jimenez/tgen/part-m-00003
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:04 /user/jimenez/tgen/part-m-00004
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:08 /user/jimenez/tgen/part-m-00005
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:08 /user/jimenez/tgen/part-m-00006
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 09:08 /user/jimenez/tgen/part-m-00007


[root@instance-1 skanduri1987]# su - hdfs
Last login: Thu May 17 08:58:48 UTC 2018 on pts/0
[hdfs@instance-1 ~]$ hadoop fsck -blocks /user/jimenez
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.
Connecting to namenode via http://instance-1.c.trusty-axe-170408.internal:50070/fsck?ugi=hdfs&blocks=1&path=%2Fuser%2Fjimenez
FSCK started by hdfs (auth:SIMPLE) from /10.142.0.2 for path /user/jimenez at Thu May 17 09:10:19 UTC 2018
.........Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      104 (avg. block size 63015384 B)
 Minimally replicated blocks:   104 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Thu May 17 09:10:19 UTC 2018 in 3 milliseconds
The filesystem under path '/user/jimenez' is HEALTHY
[hdfs@instance-1 ~]$ 