# Install nginx

## Install
```
sudo apt update
sudo apt install nginx
```


Check ufw firewall application configuration that it can detects
```
sudo ufw app list
```
| Available applications: 	|
|-------------------------	|
| Nginx Full              	|
| Nginx HTTP              	|
| Nginx HTTPS            	|
| OpenSSH                   |


## Configure ufw
```
sudo uwf allow 'Nginx Full'
```

Enable and check ufw status: 
```
sudo ufw enable
sudo ufw status
```

## Check webserver
```
systemctl status nginx
```

Type ```localhost``` in your browser address and a Welcome message from nginx should appear