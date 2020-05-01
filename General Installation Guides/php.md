# Install php

### Add PHP PPA Repository

```
sudo apt-get update
sudo apt -y install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
```

### Install Php7.4
```
sudo apt -y install php7.4
```
Check php version with: ``` php -v ``` command.


### Install some wide used extensions (this will be updated all the time)

```
sudo apt-get install -y php7.4-{bcmath,bz2,common,curl,cli,intl,gd,json,imagick,imap,mbstring,opcache,soap,mysql,pdo,xml,xmlrpc,zip}
```

### Install Php-FPM for Nginx
```
sudo apt -y install php7.4-fpm
```
Check php version with: ``` php-fpm7.4 -v ``` command.

### Edit php.ini for nginx with these commands

```
upload_max_filesize = 32M 
post_max_size = 48M 
memory_limit = 256M 
max_execution_time = 600 
max_input_vars = 3000 
max_input_time = 1000
```

Restart php fpm:
```
sudo php-fpm7.4 -t 
sudo service php7.4-fpm restart
```