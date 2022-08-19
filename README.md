# Wordpress

Deploy wordpress to a server

## Overview

1. Create a VM
2. install PHP and mySQL
3. install and configure wordpress

### Create a VM

1. install multipass locally
   `brew install multipass`
2. create an ubuntu vm
   `multipass launch --name wordpress jammy`

### install php and mysql

`sudo apt install -y mysql-client mysql-server`

```
sudo mysql -u root

mysql> CREATE DATABASE wordpressdb;

mysql> GRANT ALL PRIVILEGES ON wordpressdb.* TO "root"@"localhost";

mysql> FLUSH PRIVILEGES;

mysql> EXIT
```

`sudo apt intall -y php`

### download and install wordpress

`wget https://wordpress.org/latest.tar.gz`

explode the tar file
`tar -xzvf latest.tar.gz`

# login to the vm

`multipass shell wordpress`


sudo apt install mysql-client mysql-server
sudo apt install -y  mysql-client mysql-server
systemctl status mysql.service

10. which mysql
11. mysql
12. sudo mysql -u root
13. history
14. sudo apt install -y php
15. mysql -u root
16. sudo mysql -u root
17. php --version
18. wget https://wordpress.org/latest.tar.gz
19. tar -xzvf latest.tar.gz
20. nano wordpress/wp-config-sample.php
21. ip a
22. history
23. 
<br>
<br>

to access mysql monitor

`sudo mysql` 
<br>
<br>


first login to the database server as follows:
`sudo mysql -u root -p`

<br>
<br>

mysql> `SHOW DATABASES;`
      
      | Database |
      +--------------------+
      | information_schema |
      | mysql |
      | performance_schema |
      | sys |
      | wordpressdb |
      +--------------------+
      5 rows in set (0.01 sec)


check ip address of vm
<br>
`ip a`
<br>
// 192.168.64.2
<br>
<br>
<br>
<br>
mysql> `select current_user();`
    
      | current_user() |
      +----------------+
      | root@localhost |