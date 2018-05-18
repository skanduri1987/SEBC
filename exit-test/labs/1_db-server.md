
[root@instance-1 yum.repos.d]# hostname -f
instance-1.c.trusty-axe-170408.internal

[root@instance-1 yum.repos.d]# [root@instance-1 yum.repos.d]# hostname -f
bash: [root@instance-1: command not found
[root@instance-1 yum.repos.d]# mysql -u root -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          10
Current database:
Current user:           root@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 8 min 46 sec

Threads: 1  Questions: 40  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.076
--------------

[root@instance-1 yum.repos.d]# mysql -u root -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| sentry             |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          12
Current database:
Current user:           rman@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 9 min 31 sec

Threads: 1  Questions: 47  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.082
--------------

[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| rman               |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u hue -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          14
Current database:
Current user:           hue@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 9 min 51 sec

Threads: 1  Questions: 54  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.091
--------------

[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| rman               |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u hue -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u hive -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u hive -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          18
Current database:
Current user:           hive@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 12 min 52 sec

Threads: 1  Questions: 67  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.086
--------------

[root@instance-1 yum.repos.d]# mysql -u oozie -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| oozie              |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u oozie -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          20
Current database:
Current user:           oozie@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Current pager:          stdout
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 12 min 53 sec
Threads: 1  Questions: 74  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.095
--------------
[root@instance-1 yum.repos.d]# mysql -u sentry -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| sentry             |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u sentry -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1
Connection id:          22
Current database:
Current user:           sentry@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 12 min 53 sec
Threads: 1  Questions: 81  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.104
--------------
[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| rman               |
+--------------------+
[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"status";
[root@instance-1 yum.repos.d]# mysql -u rman -pbigdata -e"status";
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1
Connection id:          25
Current database:
Current user:           rman@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 14 min 0 sec
Threads: 1  Questions: 92  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.109
--------------
[root@instance-1 yum.repos.d]# 

[root@instance-1 yum.repos.d]# mysql -u root -pbigdata
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 130
Server version: 5.5.56-MariaDB MariaDB Server
Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
MariaDB [(none)]> 