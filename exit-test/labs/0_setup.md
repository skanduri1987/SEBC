
1. uptime for all the nodes.
[skanduri1987@instance-1 ~]$ uptime
 02:41:14 up 4 min,  1 user,  load average: 0.01, 0.03, 0.02
 [skanduri1987@instance-2 ~]$ uptime
 02:41:19 up 4 min,  1 user,  load average: 0.00, 0.02, 0.02
 [skanduri1987@instance-3 ~]$ uptime
 02:41:22 up 4 min,  1 user,  load average: 0.00, 0.01, 0.01
 [skanduri1987@instance-4 ~]$ uptime
 02:41:26 up 4 min,  1 user,  load average: 0.00, 0.02, 0.02
 skanduri1987@instance-5 ~]$ uptime
 02:41:34 up 4 min,  1 user,  load average: 0.00, 0.02, 0.02

2. Cloud Provider: google cloud.

3. Hostnames and IP Address of the Machines:
 
10.142.0.2 instance-1.c.trusty-axe-170408.internal
10.128.0.2 instance-2.c.trusty-axe-170408.internal
10.128.0.3 instance-3.c.trusty-axe-170408.internal
10.142.0.3 instance-4.c.trusty-axe-170408.internal
10.138.0.2 instance-5.c.trusty-axe-170408.internal

4. OS release & File system Details of each host 

root@instance-5 skanduri1987]# hostname -f
instance-5.c.trusty-axe-170408.internal
[root@instance-5 skanduri1987]# cat /etc/redhat-release 
CentOS Linux release 7.5.1804 (Core) 
[root@instance-5 skanduri1987]# df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  2.1G   48G   5% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
[root@instance-5 skanduri1987]# 
root@instance-4 skanduri1987]# hostname -f
instance-4.c.trusty-axe-170408.internal
[root@instance-4 skanduri1987]# cat /etc/redhat-release 
CentOS Linux release 7.5.1804 (Core) 
[root@instance-4 skanduri1987]# df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  2.0G   49G   4% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
[root@instance-4 skanduri1987]# 
[root@instance-3 skanduri1987]# hostname -f
instance-3.c.trusty-axe-170408.internal
[root@instance-3 skanduri1987]# cat /etc/redhat-release 
CentOS Linux release 7.5.1804 (Core) 
[root@instance-3 skanduri1987]# df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  2.0G   49G   4% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
[root@instance-3 skanduri1987]# 
root@instance-2 skanduri1987]# hostname -f
instance-2.c.trusty-axe-170408.internal
[root@instance-2 skanduri1987]# cat /etc/redhat-release 
CentOS Linux release 7.5.1804 (Core) 
[root@instance-2 skanduri1987]# df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  2.0G   49G   4% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000

root@instance-1 skanduri1987]# hostname -f
instance-1.c.trusty-axe-170408.internal
[root@instance-1 skanduri1987]# cat /etc/redhat-release 
CentOS Linux release 7.5.1804 (Core) 
[root@instance-1 skanduri1987]# df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  2.1G   48G   5% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
[root@instance-1 skanduri1987]# 

5. yum repolist enabled on each host:

[root@instance-1 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: centos.aol.com
 * epel: mirror.cogentco.com
 * extras: repos.mia.quadranet.com
 * updates: mirrors.advancedhosters.com
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-director                                                           Cloudera Director                                                                                          5
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
mariadb                                                                     MariaDB                                                                                                   46
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 23,014
[root@instance-1 skanduri1987]# 
[root@instance-2 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirrors.umflint.edu
 * epel: mirror.steadfast.net
 * extras: mirrors.cmich.edu
 * updates: mirrors.tummy.com
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-director                                                           Cloudera Director                                                                                          5
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
mariadb                                                                     MariaDB                                                                                                   46
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 23,014
[root@instance-2 skanduri1987]# 
[root@instance-3 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: pubmirrors.dal.corespace.com
 * epel: mirror.steadfast.net
 * extras: mirrors.cmich.edu
 * updates: mirrors.tummy.com
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-director                                                           Cloudera Director                                                                                          5
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
mariadb                                                                     MariaDB                                                                                                   46
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 23,014
[root@instance-3 skanduri1987]# 
[root@instance-4 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirrors.advancedhosters.com
 * epel: mirror.cogentco.com
 * extras: mirror.wdc1.us.leaseweb.net
 * updates: mirror.wdc1.us.leaseweb.net
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-director                                                           Cloudera Director                                                                                          5
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
mariadb                                                                     MariaDB                                                                                                   46
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 23,014
[root@instance-4 skanduri1987]# 
[root@instance-5 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.sjc02.svwh.net
 * epel: mirrors.cat.pdx.edu
 * extras: centos.eecs.wsu.edu
 * updates: centos.s.uw.edu
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-director                                                           Cloudera Director                                                                                          5
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
mariadb                                                                     MariaDB                                                                                                   46
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 23,014
[root@instance-5 skanduri1987]# 


6. Users & Group Creation evidences:

Instance -1 

tail -f /etc/passwd

thanos:x:2500:2701::/home/thanos:/bin/bash
hulk:x:2600:2702::/home/hulk:/bin/bash
groot:x:2700:2702::/home/groot:/bin/bash

[root@instance-1 skanduri1987]# tail -f /etc/group
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
nscd:x:28:
santosh:x:1002:
thanos:x:2500:
hulk:x:2600:
groot:x:2700:
blackorder:x:2701:
avengers:x:2702:


[root@instance-5 skanduri1987]# tail -f /etc/passwd
ntp:x:38:38::/etc/ntp:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
nscd:x:28:28:NSCD Daemon:/:/sbin/nologin
santosh:x:1001:1002::/home/santosh:/bin/bash
thanos:x:2500:2701::/home/thanos:/bin/bash
hulk:x:2600:2702::/home/hulk:/bin/bash
groot:x:2700:2702::/home/groot:/bin/bash
^C
[root@instance-5 skanduri1987]# tail -f /etc/group
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
nscd:x:28:
santosh:x:1002:
thanos:x:2500:
hulk:x:2600:
groot:x:2700:
blackorder:x:2701:
avengers:x:2702:


[root@instance-2 skanduri1987]# tail -f /etc/passwd
ntp:x:38:38::/etc/ntp:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
nscd:x:28:28:NSCD Daemon:/:/sbin/nologin
santosh:x:1001:1002::/home/santosh:/bin/bash
thanos:x:2500:2701::/home/thanos:/bin/bash
hulk:x:2600:2702::/home/hulk:/bin/bash
groot:x:2700:2702::/home/groot:/bin/bash
^C
[root@instance-2 skanduri1987]# tail -f /etc/group
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
nscd:x:28:
santosh:x:1002:
thanos:x:2500:
hulk:x:2600:
groot:x:2700:
blackorder:x:2701:
avengers:x:2702:

[root@instance-3 skanduri1987]# tail -f /etc/passwd
ntp:x:38:38::/etc/ntp:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
nscd:x:28:28:NSCD Daemon:/:/sbin/nologin
santosh:x:1001:1002::/home/santosh:/bin/bash
thanos:x:2500:2701::/home/thanos:/bin/bash
hulk:x:2600:2702::/home/hulk:/bin/bash
groot:x:2700:2702::/home/groot:/bin/bash
^C
[root@instance-3 skanduri1987]# tail -f /etc/group
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
nscd:x:28:
santosh:x:1002:
thanos:x:2500:
hulk:x:2600:
groot:x:2700:
blackorder:x:2701:
avengers:x:2702:

root@instance-4 skanduri1987]# tail -f /etc/passwd
ntp:x:38:38::/etc/ntp:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
nscd:x:28:28:NSCD Daemon:/:/sbin/nologin
santosh:x:1001:1002::/home/santosh:/bin/bash
thanos:x:2500:2701::/home/thanos:/bin/bash
hulk:x:2600:2702::/home/hulk:/bin/bash
groot:x:2700:2702::/home/groot:/bin/bash
^C
[root@instance-4 skanduri1987]# tail -f /etc/group
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
nscd:x:28:
santosh:x:1002:
thanos:x:2500:
hulk:x:2600:
groot:x:2700:
blackorder:x:2701:
avengers:x:2702:

