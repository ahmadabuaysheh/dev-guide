# Install Node and npm

Beaware that number 12 can change based on the [current version of node](https://nodejs.org/en/download/), we are choosing the LTS version here since it's the most stable one to use. You can instal the cuurent version by changin 12 to 14 in this case. But always check the majot version in the aforementioned link.

```Shell
cd ~
curl -sL https://deb.nodesource.com/setup_14.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs
```

Check node and npm versions:
```
node -v
npm -v
```