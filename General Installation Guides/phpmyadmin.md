# Installation of phpmyadmin

This tool depends on: Nginx, php and mysql

### Clone the phpmyadmin project into your main projects folder

```
composer create-project phpmyadmin/phpmyadmin
```

### Since this project is a php project we need to point the nginx to it.

Edit Host: ``` sudo vim /etc/hosts ```

Add the following line to host: ``` 127.0.0.1  pma.local.test ```

### copy phpmyadmin.conf to sites-available and link it in the sites-enabled folder

### Open ```pma.local.test``` in your browser

### Assign a blowfish secret in the config file

```
cp config.sample.inc.php config.inc.php
vim config.inc.php
```

### if phpmyadmin shows a cache problem, add the current user to the www-data group

```
sudo adduser $USER www-data  
```

and for the files, change the group to www-data instead of user
```
sudo chown -R $USER:www-data *
```