
 
1. Cloud Provider : Google Cloud.

2. Linux Release : centos7 64bit.

3. List All Instances:
 
 10.142.0.2 instance-1.c.trusty-axe-170408.internal
 10.142.0.3 instance-3.c.trusty-axe-170408.internal
 10.128.0.2 instance-3.c.trusty-axe-170408.internal
 10.128.0.3 instance-4.c.trusty-axe-170408.internal
 10.138.0.2 instance-5.c.trusty-axe-170408.internal

3. Filesystem Details 

[skanduri1987@instance-1 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/sda1      xfs        50G  1.5G   49G   3% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.3G     0  7.3G   0% /dev/shm
tmpfs          tmpfs     7.3G  9.4M  7.3G   1% /run
tmpfs          tmpfs     7.3G     0  7.3G   0% /sys/fs/cgroup
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000

4. yum repolist Enabled. 

[root@instance-1 skanduri1987]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.osuosl.org
 * epel: reflector.westga.edu
 * extras: mirror.wdc1.us.leaseweb.net
 * updates: distro.ibiblio.org
repo id                                                                     repo name                                                                                             status
base/7/x86_64                                                               CentOS-7 - Base                                                                                        9,911
cloudera-manager                                                            Cloudera Manager, Version 5.13.3.2                                                                         7
epel/x86_64                                                                 Extra Packages for Enterprise Linux 7 - x86_64                                                        12,542
extras/7/x86_64                                                             CentOS-7 - Extras                                                                                        258
google-cloud-compute                                                        Google Cloud Compute                                                                                       9
google-cloud-sdk                                                            Google Cloud SDK                                                                                          92
updates/7/x86_64                                                            CentOS-7 - Updates                                                                                       151
repolist: 22,970
[root@instance-1 skanduri1987]# 

5. User Creation

root@instance-1 skanduri1987]# tail -f /etc/passwd
systemd-network:x:192:192:systemd Network Management:/:/sbin/nologin
dbus:x:81:81:System message bus:/:/sbin/nologin
polkitd:x:999:997:User for polkitd:/:/sbin/nologin
ntp:x:38:38::/etc/ntp:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
jimenez:x:2800:2800::/home/jimenez:/bin/bash
beltran:x:2900:2900::/home/beltran:/bin/bash
^C
[root@instance-1 skanduri1987]# groupadd astros
[root@instance-1 skanduri1987]# groupadd rangers
[root@instance-1 skanduri1987]# usermod -g astros jimenez
[root@instance-1 skanduri1987]# usermod -g rangers beltran 
[root@instance-1 skanduri1987]# tail -f /etc/passwd
systemd-network:x:192:192:systemd Network Management:/:/sbin/nologin
dbus:x:81:81:System message bus:/:/sbin/nologin
polkitd:x:999:997:User for polkitd:/:/sbin/nologin
ntp:x:38:38::/etc/ntp:/sbin/nologin
postfix:x:89:89::/var/spool/postfix:/sbin/nologin
sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
chrony:x:998:996::/var/lib/chrony:/sbin/nologin
skanduri1987:x:1000:1001::/home/skanduri1987:/bin/bash
jimenez:x:2800:2901::/home/jimenez:/bin/bash
beltran:x:2900:2902::/home/beltran:/bin/bash
^C
[root@instance-1 skanduri1987]# tail -f /etc/group
postfix:x:89:
sshd:x:74:
chrony:x:996:
cgred:x:995:
google-sudoers:x:1000:skanduri1987
skanduri1987:x:1001:
jimenez:x:2800:
beltran:x:2900:
astros:x:2901:
rangers:x:2902:
^C
[root@instance-1 skanduri1987]# id jimenez
uid=2800(jimenez) gid=2901(astros) groups=2901(astros)
[root@instance-1 skanduri1987]# id beltran
uid=2900(beltran) gid=2902(rangers) groups=2902(rangers)
useradd -u 2800 jimenez
useradd -u 2900 beltran
groupadd astros
groupadd rangers
usermod -g astros jimenez
usermod -g rangers beltran
 
