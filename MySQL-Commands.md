# Create User
> CREATE USER 'user'@'%' IDENTIFIED BY 'pass';
> 
> GRANT SELECT,INSERT,DELETE,CREATE,DROP,UPDATE,ALTER ON test_app.* to 'user'@'%' IDENTIFIED BY 'pass';
> 
> flush privileges;

# Update password
> SET PASSWORD FOR 'reader'@'%' = PASSWORD('12345');

# MySQL Dump
> mysqldump --user=user --password=pass-f  conf_db  --ignore-table=conf_db.event_history  > /home/mysql_confdb_backup.sql

# Optimize table size
> optimize table table_name;

# Checking any column exist or not
> SELECT EXISTS(SELECT 1 FROM hosts WHERE address = "xxx") AS myCheck 
