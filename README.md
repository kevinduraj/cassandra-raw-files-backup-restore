Cassandra Data Directory Backup/Restore
=======================================

###Perform Task on Each Node of the Cluster

* 0-backup-cassandra.sh - (Source Node) 
  * copy Cassandra raw direrectory with files into desctination using rsync

* 1-downgrade-dse.sh - (Optional if version differs - Destination Node) 
  * downgrade Cassandra to the source version 4.8.4 
  * ls -l /user/share/dse

* 2-update-system.sh - (Destination Node) 
  * update Cassandra yaml files and system tables

* 3-delete-peers.sh - (Detination Node) 
  * delete peers

### Bash Aliases 

```
$ vi ~/.bash_aliases
  alias 1='tail -50f /var/log/cassandra/output.log'
  alias 2='tail -50f /var/log/cassandra/system.log'
```

###References:
[https://github.com/richrein/cassandra.bin](https://github.com/richrein/cassandra.bin)
