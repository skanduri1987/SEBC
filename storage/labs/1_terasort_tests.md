Teragen & Tera sort LAB:

[hdfs@instance-1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen  -Dmapred.map.tasks=4  -Ddfs.block.size=33554432 1000000 /user/skand
uri1987/teragentest
18/05/15 03:51:33 INFO client.RMProxy: Connecting to ResourceManager at instance-3.c.trusty-axe-170408.internal/10.128.0.3:8032
18/05/15 03:51:35 INFO terasort.TeraGen: Generating 1000000 using 4
18/05/15 03:51:37 INFO mapreduce.JobSubmitter: number of splits:4
18/05/15 03:51:37 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/15 03:51:37 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/15 03:51:38 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526282844097_0221
18/05/15 03:51:39 INFO impl.YarnClientImpl: Submitted application application_1526282844097_0221
18/05/15 03:51:39 INFO mapreduce.Job: The url to track the job: http://instance-3.c.trusty-axe-170408.internal:8088/proxy/application_1526282844097_0221/
18/05/15 03:51:39 INFO mapreduce.Job: Running job: job_1526282844097_0221
18/05/15 03:51:47 INFO mapreduce.Job: Job job_1526282844097_0221 running in uber mode : false
18/05/15 03:51:47 INFO mapreduce.Job:  map 0% reduce 0%
18/05/15 03:51:58 INFO mapreduce.Job:  map 75% reduce 0%
18/05/15 03:52:04 INFO mapreduce.Job:  map 100% reduce 0%
18/05/15 03:52:09 INFO mapreduce.Job: Job job_1526282844097_0221 completed successfully
18/05/15 03:52:09 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=605743
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=337
                HDFS: Number of bytes written=100000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters 
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=39129
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=39129
                Total vcore-milliseconds taken by all map tasks=39129
                Total megabyte-milliseconds taken by all map tasks=40068096
        Map-Reduce Framework
                Map input records=1000000
                Map output records=1000000
                Input split bytes=337
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=495
                CPU time spent (ms)=7600
                Physical memory (bytes) snapshot=1062350848
                Virtual memory (bytes) snapshot=11166339072
                Total committed heap usage (bytes)=1183318016
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=2148987642402270
        File Input Format Counters 
                Bytes Read=0
        File Output Format Counters 
                Bytes Written=100000000
real    0m37.999s
user    0m6.689s
sys     0m0.435s


Terasort Execution 

[hdfs@instance-1 ~]$ time yarn jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  terasort  /user/skanduri1987/teragentest /user/skanduri1987/terasortoutput
18/05/15 03:59:01 INFO terasort.TeraSort: starting
18/05/15 03:59:02 INFO input.FileInputFormat: Total input paths to process : 4
Spent 298ms computing base-splits.
Spent 37ms computing TeraScheduler splits.
Computing input splits took 335ms
Sampling 4 splits of 4
Making 6 from 100000 sampled records
Computing parititions took 2778ms
Spent 3115ms computing partitions.
18/05/15 03:59:05 INFO client.RMProxy: Connecting to ResourceManager at instance-3.c.trusty-axe-170408.internal/10.128.0.3:8032
18/05/15 03:59:09 INFO mapreduce.JobSubmitter: number of splits:4
18/05/15 03:59:10 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526282844097_0222
18/05/15 03:59:11 INFO impl.YarnClientImpl: Submitted application application_1526282844097_0222
18/05/15 03:59:11 INFO mapreduce.Job: The url to track the job: http://instance-3.c.trusty-axe-170408.internal:8088/proxy/application_1526282844097_0222/
18/05/15 03:59:11 INFO mapreduce.Job: Running job: job_1526282844097_0222
18/05/15 03:59:19 INFO mapreduce.Job: Job job_1526282844097_0222 running in uber mode : false
18/05/15 03:59:19 INFO mapreduce.Job:  map 0% reduce 0%
18/05/15 03:59:27 INFO mapreduce.Job:  map 25% reduce 0%
18/05/15 03:59:28 INFO mapreduce.Job:  map 100% reduce 0%
18/05/15 03:59:38 INFO mapreduce.Job:  map 100% reduce 17%
18/05/15 03:59:39 INFO mapreduce.Job:  map 100% reduce 50%
18/05/15 03:59:45 INFO mapreduce.Job:  map 100% reduce 100%
18/05/15 03:59:49 INFO mapreduce.Job: Job job_1526282844097_0222 completed successfully
18/05/15 03:59:50 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=43313803
                FILE: Number of bytes written=88191477
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=100000508
                HDFS: Number of bytes written=100000000
                HDFS: Number of read operations=30
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters 
                Launched map tasks=4
                Launched reduce tasks=6
                Data-local map tasks=3
                Rack-local map tasks=1
                Total time spent by all maps in occupied slots (ms)=26028
                Total time spent by all reduces in occupied slots (ms)=65403
                Total time spent by all map tasks (ms)=26028
                Total time spent by all reduce tasks (ms)=65403
                Total vcore-milliseconds taken by all map tasks=26028
                Total vcore-milliseconds taken by all reduce tasks=65403
                Total megabyte-milliseconds taken by all map tasks=26652672
                Total megabyte-milliseconds taken by all reduce tasks=66972672
        Map-Reduce Framework
                Map input records=1000000
                Map output records=1000000
                Map output bytes=102000000
                Map output materialized bytes=43347671
                Input split bytes=508
                Combine input records=0
                Combine output records=0
                Reduce input groups=1000000
                Reduce shuffle bytes=43347671
                Reduce input records=1000000
                Reduce output records=1000000
                Spilled Records=2000000
                Shuffled Maps =24
                Failed Shuffles=0
                Merged Map outputs=24
                GC time elapsed (ms)=1476
                CPU time spent (ms)=30460
                Physical memory (bytes) snapshot=3633967104
                Virtual memory (bytes) snapshot=28036939776
                Total committed heap usage (bytes)=3793223680
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters 
                Bytes Read=100000000
        File Output Format Counters 
                Bytes Written=100000000
18/05/15 03:59:50 INFO terasort.TeraSort: done
real    0m49.437s
user    0m7.373s
sys     0m0.397s
