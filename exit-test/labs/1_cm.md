[cloudera-manager]
name = Cloudera Manager, Version 5.11.2
baseurl = https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.11.2/
gpgkey = https://archive.cloudera.com/redhat/cdh/RPM-GPG-KEY-cloudera
gpgcheck = 1

[root@instance-2 yum.repos.d]# yum list all | grep cloudera
oracle-j2sdk1.8.x86_64                    1.8.0+update121-1            @cloudera-director
cloudera-director-client.x86_64           2.7.1-1.director271.p0.28.el7
                                                                       cloudera-director
cloudera-director-plugins.x86_64          2.7.1-1.director271.p0.28.el7
                                                                       cloudera-director
cloudera-director-server.x86_64           2.7.1-1.director271.p0.28.el7
                                                                       cloudera-director
cloudera-manager-agent.x86_64             5.11.2-1.cm5112.p0.6.el7     cloudera-manager
cloudera-manager-daemons.x86_64           5.11.2-1.cm5112.p0.6.el7     cloudera-manager
cloudera-manager-server.x86_64            5.11.2-1.cm5112.p0.6.el7     cloudera-manager
cloudera-manager-server-db-2.x86_64       5.11.2-1.cm5112.p0.6.el7     cloudera-manager
enterprise-debuginfo.x86_64               5.11.2-1.cm5112.p0.6.el7     cloudera-manager
jdk.x86_64                                2000:1.6.0_31-fcs            cloudera-manager
oracle-j2sdk1.7.x86_64                    1.7.0+update67-1      

