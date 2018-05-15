Snapshot in HDFS

1. Create a Directory /user/precious and copy SEBC.zip files to hdfs using below command
     
     hdfs dfs -mkdir /user/precious
     hdfs dfs -put SEBC.zip /user/precious

     validate :

     hdfs dfs -ls /user/precious/
     
	     [hdfs@instance-1 tmp]$ hdfs dfs -ls /user/precious
		  Found 1 items
		   rw-r--rwxr-xr-x   3 hdfs supergroup     471851 2018-05-15 04:07 /user/precious/SEBC.zip


 2. Allow snapshots
    
[hdfs@instance-1 tmp]$ hdfs dfsadmin -allowSnapshot /user/precious/
Allowing snaphot on /user/precious/ succeeded

3. Create snapshot 

[hdfs@instance-1 tmp]$ hdfs dfs -createSnapshot /user/precious/
Created snapshot /user/precious/.snapshot/s20180515-040954.550

4. List the snapshot directory

[hdfs@instance-1 tmp]$ hdfs dfs -ls /user/precious/.snapshot/s20180515-040954.550
Found 1 items
-rwxr-xr-x   3 hdfs supergroup     471851 2018-05-15 04:07 /user/precious/.snapshot/s20180515-040954.550/SEBC.zip

5. Remove the file manually and recover it from snapshot:

[hdfs@instance-1 tmp]$ hdfs dfs -rm -r /user/precious/SEBC.zip
18/05/15 04:12:09 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/precious/SEBC.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/precious/SEBC.zip
  validate the file deletion. 

[hdfs@instance-1 tmp]$ hdfs dfs -ls /user/precious
[hdfs@instance-1 tmp]$ hdfs dfs -ls /user/precious
   
 6. Recover the File from snap shot:

[hdfs@instance-1 tmp]$ hdfs dfs -cp /user/precious/.snapshot/s20180515-040954.550/SEBC.zip /user/precious/
[hdfs@instance-1 tmp]$ hdfs dfs -ls /user/precious/
Found 2 items
-rw-r--r--   3 hdfs supergroup     471851 2018-05-15 04:13 /user/precious/SEBC.zip
