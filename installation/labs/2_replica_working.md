mysql> SHOW SLAVE STATUS \G

	*************************** 1. row ***************************

               Slave_IO_State: Waiting for master to send event
                  Master_Host: 172.31.1.96
                  Master_User: repl
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysql-bin.000003
          Read_Master_Log_Pos: 1637
               Relay_Log_File: mysqld-relay-bin.000002
                Relay_Log_Pos: 253
        Relay_Master_Log_File: mysql-bin.000003
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB: 
          Replicate_Ignore_DB: 
           Replicate_Do_Table: 
       Replicate_Ignore_Table: 
      Replicate_Wild_Do_Table: 
	Replicate_Wild_Ignore_Table: 
                   Last_Errno: 0
                   Last_Error: 
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 1637
              Relay_Log_Space: 410
              Until_Condition: None
               Until_Log_File: 
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File: 
           Master_SSL_CA_Path: 
              Master_SSL_Cert: 
            Master_SSL_Cipher: 
               Master_SSL_Key: 
        Seconds_Behind_Master: 0
	Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error: 
               Last_SQL_Errno: 0
               Last_SQL_Error: 
  	Replicate_Ignore_Server_Ids: 
             Master_Server_Id: 1
1 row in set (0.00 sec)

Review your log (/var/log/mysqld.log) for errors. If stuck, consult with a colleague or instructor.

	[root@ip-172-31-15-67 ~]#tail -n 3 /var/log/mysqld.log
	170508 16:09:42 [Note] 'CHANGE MASTER TO executed'. Previous state master_host='', master_port='3306', master_log_file='', master_log_pos='4'. New state master_host='172.31.1.96', master_port='3306', master_log_file='mysql-bin.000003', master_log_pos='1637'.
	170508 16:09:57 [Note] Slave SQL thread initialized, starting replication in log 'mysql-bin.000003' at position 1637, relay log './mysqld-relay-bin.000001' position: 4
	170508 16:09:57 [Note] Slave I/O thread: connected to master 'repl@172.31.1.96:3306',replication started in log 'mysql-bin.000003' at position 1637
