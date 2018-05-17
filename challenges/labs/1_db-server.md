
[root@instance-1 skanduri1987]# hostname -f
instance-1.c.trusty-axe-170408.internal

[root@instance-1 skanduri1987]# mysql -u root -p 
Enter password: 
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 10
Server version: 5.5.56-MariaDB MariaDB Server

Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> grant all on *.* ro 'root'@'%' identified by 'bigdata';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'ro 'root'@'%' identified by 'bigdata'' at line 1
MariaDB [(none)]> grant all on *.* to 'root'@'%' identified by 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database amondb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on amondb.* TO 'amon'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database rmandb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on rmandb.* TO 'rman'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database metastore DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database huedb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database ooziedb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on ooziedb.* TO 'oozie'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database navdb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on navdb.* TO 'nav'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> create database navmsdb DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> grant all on navmsdb.* TO 'navms'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> flush privileges;
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> Bye
[root@instance-1 skanduri1987]# hostname -f
instance-1.c.trusty-axe-170408.internal
[root@instance-1 skanduri1987]# mysql -u root -pbigdata -e "status"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          11
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
Uptime:                 19 min 36 sec

Threads: 1  Questions: 43  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.036
--------------

[root@instance-1 skanduri1987]# mysql -u amon -pbigdata -e "status"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          12
Current database:
Current user:           amon@localhost
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
Uptime:                 19 min 51 sec

Threads: 1  Questions: 47  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.039
--------------

[root@instance-1 skanduri1987]# mysql -u rman -pbigdata -e "status"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          13
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
Uptime:                 20 min 0 sec

Threads: 1  Questions: 51  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.042
--------------

[root@instance-1 skanduri1987]# mysql -u nav -pbigdata -e "status"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          14
Current database:
Current user:           nav@localhost
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
Uptime:                 20 min 10 sec

Threads: 1  Questions: 55  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.045
--------------

[root@instance-1 skanduri1987]# mysql -u navms -pbigdata -e "status"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          15
Current database:
Current user:           navms@localhost
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
Uptime:                 20 min 16 sec

Threads: 1  Questions: 59  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.048
--------------

[root@instance-1 skanduri1987]# mysql -u root -p
Enter password: 
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 16
Server version: 5.5.56-MariaDB MariaDB Server

Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database sentry DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database hue DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database oozie DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database hive DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> create database rman DEFAULT CHARACTER SET utf8;
Query OK, 1 row affected (0.00 sec)

MariaDB [(none)]> flush privileges;
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> Bye
[root@instance-1 skanduri1987]# mysql -u root -pbigdata -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amondb             |
| hive               |
| hue                |
| huedb              |
| metastore          |
| mysql              |
| navdb              |
| navmsdb            |
| oozie              |
| ooziedb            |
| performance_schema |
| rman               |
| rmandb             |
| sentry             |
+--------------------+
[root@instance-1 skanduri1987]# mysql -u root -p
Enter password: 
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 18
Server version: 5.5.56-MariaDB MariaDB Server
Copyright (c) 2000, 2017, Oracle, MariaDB Corporation Ab and others.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
MariaDB [(none)]> drop database huedb;
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> drop database amondb;
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> drop database rmandb;
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> drop database metastore;
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> grant all on oozie.* TO 'oozie'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> grant all on hive.* TO 'hive'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'bigdata';
Query OK, 0 rows affected (0.00 sec)
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| navdb              |
| navmsdb            |
| oozie              |
| ooziedb            |
| performance_schema |
| rman               |
| sentry             |
+--------------------+
11 rows in set (0.00 sec)
MariaDB [(none)]> 
