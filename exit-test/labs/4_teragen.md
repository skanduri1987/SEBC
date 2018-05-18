time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen  -Dmapred.map.tasks=40  -Ddfs.block.size=67108864  5242880 /user/groot/tgen

O/P


groot@instance-1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen  -Dmapred.map.tasks=40  -Ddfs.block.size=67108864  5242880 /user/gr
oot/tgen
18/05/18 05:19:38 INFO client.RMProxy: Connecting to ResourceManager at instance-1.c.trusty-axe-170408.internal/10.142.0.2:8032
18/05/18 05:19:40 INFO terasort.TeraGen: Generating 5242880 using 40
18/05/18 05:19:42 INFO mapreduce.JobSubmitter: number of splits:40
18/05/18 05:19:42 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/18 05:19:42 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/18 05:19:43 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526619163590_0001
18/05/18 05:19:43 INFO impl.YarnClientImpl: Submitted application application_1526619163590_0001
18/05/18 05:19:43 INFO mapreduce.Job: The url to track the job: http://instance-1.c.trusty-axe-170408.internal:8088/proxy/application_1526619163590_0001/
18/05/18 05:19:43 INFO mapreduce.Job: Running job: job_1526619163590_0001
18/05/18 05:19:51 INFO mapreduce.Job: Job job_1526619163590_0001 running in uber mode : false
18/05/18 05:19:51 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:20:05 INFO mapreduce.Job:  map 8% reduce 0%
18/05/18 05:20:07 INFO mapreduce.Job:  map 10% reduce 0%
18/05/18 05:20:08 INFO mapreduce.Job:  map 15% reduce 0%
18/05/18 05:20:09 INFO mapreduce.Job:  map 17% reduce 0%
18/05/18 05:20:10 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 05:20:14 INFO mapreduce.Job:  map 21% reduce 0%
18/05/18 05:20:15 INFO mapreduce.Job:  map 24% reduce 0%
18/05/18 05:20:19 INFO mapreduce.Job:  map 26% reduce 0%
18/05/18 05:20:20 INFO mapreduce.Job:  map 34% reduce 0%
18/05/18 05:20:21 INFO mapreduce.Job:  map 36% reduce 0%
18/05/18 05:20:24 INFO mapreduce.Job:  map 39% reduce 0%
18/05/18 05:20:26 INFO mapreduce.Job:  map 41% reduce 0%
18/05/18 05:20:27 INFO mapreduce.Job:  map 44% reduce 0%
18/05/18 05:20:30 INFO mapreduce.Job:  map 46% reduce 0%
18/05/18 05:20:31 INFO mapreduce.Job:  map 49% reduce 0%
18/05/18 05:20:32 INFO mapreduce.Job:  map 54% reduce 0%
18/05/18 05:20:33 INFO mapreduce.Job:  map 56% reduce 0%
18/05/18 05:20:35 INFO mapreduce.Job:  map 59% reduce 0%
18/05/18 05:20:43 INFO mapreduce.Job:  map 64% reduce 0%
18/05/18 05:20:45 INFO mapreduce.Job:  map 69% reduce 0%
18/05/18 05:20:46 INFO mapreduce.Job:  map 74% reduce 0%
18/05/18 05:20:47 INFO mapreduce.Job:  map 76% reduce 0%
18/05/18 05:20:48 INFO mapreduce.Job:  map 79% reduce 0%
18/05/18 05:20:55 INFO mapreduce.Job:  map 81% reduce 0%
18/05/18 05:20:57 INFO mapreduce.Job:  map 84% reduce 0%
18/05/18 05:20:58 INFO mapreduce.Job:  map 87% reduce 0%
18/05/18 05:20:59 INFO mapreduce.Job:  map 89% reduce 0%
18/05/18 05:21:00 INFO mapreduce.Job:  map 92% reduce 0%
18/05/18 05:21:01 INFO mapreduce.Job:  map 94% reduce 0%
18/05/18 05:21:02 INFO mapreduce.Job:  map 97% reduce 0%
18/05/18 05:21:08 INFO mapreduce.Job:  map 99% reduce 0%
18/05/18 05:21:46 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 05:24:16 INFO mapreduce.Job: Job job_1526619163590_0001 completed successfully
18/05/18 05:24:16 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=5189830
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=3397
                HDFS: Number of bytes written=524288000
                HDFS: Number of read operations=160
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=80
        Job Counters 
                Launched map tasks=40
                Other local map tasks=40
                Total time spent by all maps in occupied slots (ms)=742197
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=742197
                Total vcore-milliseconds taken by all map tasks=742197
                Total megabyte-milliseconds taken by all map tasks=760009728
        Map-Reduce Framework
                Map input records=5242880
                Map output records=5242880
                Input split bytes=3397
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=5210
                CPU time spent (ms)=65370
                Physical memory (bytes) snapshot=9438007296
                Virtual memory (bytes) snapshot=111351083008
                Total committed heap usage (bytes)=10233053184
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=11257830824958050
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=524288000
real    4m40.445s
user    0m9.110s
sys     0m0.626s
[groot@instance-1 ~]$ 



[groot@instance-1 ~]$ hdfs dfs -ls /user/groot/tgen
Found 41 items
-rw-r--r--   3 groot supergroup          0 2018-05-18 05:24 /user/groot/tgen/_SUCCESS
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00000
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00001
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00002
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00003
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00004
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00005
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00006
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00007
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:24 /user/groot/tgen/part-m-00008
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00009
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00010
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00011
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00012
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00013
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00014
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00015
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00016
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00017
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00018
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00019
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00020
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00021
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00022
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00023
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00024
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00025
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00026
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00027
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00028
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00029
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00030
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00031
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00032
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00033
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00034
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:21 /user/groot/tgen/part-m-00035
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00036
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00037
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:20 /user/groot/tgen/part-m-00038
-rw-r--r--   3 groot supergroup   13107200 2018-05-18 05:21 /user/groot/tgen/part-m-00039

[root@instance-1 skanduri1987]# su - hdfs
Last login: Fri May 18 05:19:13 UTC 2018 on pts/0
[hdfs@instance-1 ~]$ hadoop fsck -blocks /user/groot
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.
Connecting to namenode via http://instance-1.c.trusty-axe-170408.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /10.142.0.2 for path /user/groot at Fri May 18 05:26:42 UTC 2018
.........................................Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    3
 Total files:   41
 Total symlinks:                0
 Total blocks (validated):      40 (avg. block size 13107200 B)
 Minimally replicated blocks:   40 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri May 18 05:26:42 UTC 2018 in 7 milliseconds
The filesystem under path '/user/groot' is HEALTHY
[hdfs@instance-1 ~]$ 
