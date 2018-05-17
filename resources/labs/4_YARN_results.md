Last login: Wed May 16 06:54:43 2018 from 173.194.93.33
[skanduri1987@instance-1 ~]$ cd /opt/
[skanduri1987@instance-1 opt]$ vi yarntest.sh
[skanduri1987@instance-1 opt]$ sudo bash
[root@instance-1 opt]# cd /tmp/
[root@instance-1 tmp]# vi yarntest.sh
[root@instance-1 tmp]# chmod u+x yarntest.sh 
[root@instance-1 tmp]# ./yarntest.sh 
Testing loop started on Wed May 16 10:05:43 UTC 2018



^C
real    0m20.230s
user    0m6.212s
sys     0m0.458s

real    0m2.146s
user    0m2.778s
sys     0m0.201s
rm: `/results/tg-10GB-8-1-512': No such file or directory
#!/bin/sh
rm: `/results/ts-10GB-8-1-512': No such file or directory
#!/bin/sh



real    0m31.548s
user    0m7.083s
sys     0m0.373s

real    0m2.180s
user    0m2.840s
sys     0m0.217s
rm: `/results/tg-10GB-8-1-1024': No such file or directory
rm: `/results/ts-10GB-8-1-1024': No such file or directory
Testing loop ended on Wed May 16 10:06:48 UTC 2018
[root@instance-1 tmp]# 
[root@instance-1 tmp]# 
[root@instance-1 tmp]# vi yarntest.sh 
[root@instance-1 tmp]# hdfs dfs -ls /
Found 2 items
drwxrwxrwt   - hdfs supergroup          0 2018-05-14 10:51 /tmp
drwxrwxrwx   - hdfs supergroup          0 2018-05-16 10:05 /user
[root@instance-1 tmp]# su - hdfs 
Last login: Wed May 16 01:36:37 UTC 2018 on pts/0
[hdfs@instance-1 ~]$ hdfs dfs -mkdir /results
[hdfs@instance-1 ~]$ hdfs dfs -chmod -R 777 /results
[hdfs@instance-1 ~]$ logout
[root@instance-1 tmp]# ./yarntest.sh 
Testing loop started on Wed May 16 10:10:32 UTC 2018
real    2m21.006s
user    0m6.612s
sys     0m0.391s
real    5m26.479s
user    0m8.367s
sys     0m0.592s
Deleted /results/tg-10GB-8-1-512
Deleted /results/ts-10GB-8-1-512
real    2m15.364s
user    0m7.776s
sys     0m0.418s
real    5m48.424s
user    0m9.137s
sys     0m0.600s
Deleted /results/tg-10GB-8-1-1024
Deleted /results/ts-10GB-8-1-1024
Testing loop ended on Wed May 16 10:26:32 UTC 2018
[root@instance-1 tmp]# 
[root@instance-1 tmp]# vi yarntest.sh 
[root@instance-1 tmp]# vi yarntest.sh 
[root@instance-1 tmp]# ./yarntest.sh 
Testing loop started on Wed May 16 10:35:35 UTC 2018
Time Taken for Executing Teragen with container allocation 256
real    2m2.729s
user    0m7.353s
sys     0m0.501s
Time Taken for Executing Teragen with container allocation 256
real    1m23.926s
user    0m10.732s
sys     0m0.592s
Deleted /results/tg-10GB-8-1-256
Deleted /results/ts-10GB-8-1-256
Time Taken for Executing Teragen with container allocation 1280
real    2m39.070s
user    0m8.781s
sys     0m0.546s
Time Taken for Executing Teragen with container allocation 1280
real    7m1.007s
user    0m12.312s
sys     0m0.886s
Deleted /results/tg-10GB-8-1-1280
Deleted /results/ts-10GB-8-1-1280
Testing loop ended on Wed May 16 10:48:52 UTC 2018
[root@instance-1 tmp]# 