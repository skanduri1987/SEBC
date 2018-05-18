As discussed i have used base repo to install mariadb 5.5

command :

yum install mariadb-server

systemctl start maraidb
systemctl enable mariadb

validation:

[root@instance-1 yum.repos.d]# netstat -tulpn| grep 3306
tcp        0      0 10.142.0.2:3306         0.0.0.0:*               LISTEN      2030/mysqld  