# Install mysql

### Download mysql
The following command will install the latest mysql version which is 8.0 until the commit date of this file.

```
sudo apt update
sudo apt install mysql-server
```

### Install mysql
```
sudo mysql_secure_installation
```
Follow the instruction and setup the mysql server as you like. And don't forget the password you will enter since it will the main one for you. 

### To test installation
```
mysql --version
```

### Can't Access root user unless sudo

```
sudo mysql -u root -p
```
 
After you login: 

```
DROP USER 'root'@'localhost';
CREATE USER 'root'@'%' IDENTIFIED BY 'Password$';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

