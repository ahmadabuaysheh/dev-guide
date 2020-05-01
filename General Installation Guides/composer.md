# Composer installation guide

### The following command has a hash384 verifier for the installation file which changes with each update of composer. [Composer Official Installation URL](https://getcomposer.org/download/)

_This script doesn't verify the hash so I don't recommend copying it from here and use it on your own risk. Use the aforementioned link instead._

```Shell
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
# php -r "if (hash_file('sha384', 'composer-setup.php') === 'e0012edf3e80b6978849f5eff0d4b4e4c79ff1609dd1e613307e16318854d24ae64f26d17af3ef0bf7cfb710ca74755a') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

