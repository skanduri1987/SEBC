
Instance -2 : ls /etc/yum.repos.d/

[root@instance-2 skanduri1987]# ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo    CentOS-Vault.repo      epel.repo          google-cloud.repo
CentOS-CR.repo    CentOS-fasttrack.repo  CentOS-Sources.repo  cloudera-manager.repo  epel-testing.repo

/usr/share/cmf/schema/scm_prepare_database.sh mysql -h instance-1.c.trusty-axe-170408.internal -utemp -ptemp --scm-host instance-2.c.trusty-axe-170408.internal scm scm scm 

O/P 
[root@instance-2 skanduri1987]# /usr/share/cmf/schema/scm_prepare_database.sh mysql -h instance-1.c.trusty-axe-170408.internal -utemp -ptemp --scm-host instance-2.c.trusty-axe-170408.i
nternal scm scm scm
JAVA_HOME=/usr/java/jdk1.8.0_161
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_161/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterpris
e.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!