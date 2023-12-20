# Create User
> CREATE USER 'user'@'%' IDENTIFIED BY 'pass';
> 
> GRANT SELECT,INSERT,DELETE,CREATE,DROP,UPDATE,ALTER ON test_app.* to 'user'@'%' IDENTIFIED BY 'pass';
> 
> flush privileges;

# Update password
> SET PASSWORD FOR 'reader'@'%' = PASSWORD('12345');
