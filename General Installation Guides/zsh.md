# Install zsh termainal with a theme and proper configurations

## Useful refrences
[Install Reference](http://jr0cket.co.uk/2017/08/beautiful-terminalation-ohmyzsh-on-ubuntu.html)

[Refrence for powerlevel10](https://drasite.com/blog/Pimp%20my%20terminal)

[powerlink10k github repo](https://github.com/romkatv/powerlevel10k/blob/master/README.md)


## Steps:

### Install zsh
```Shell
sudo apt install zsh
```

### Install ohmyzsh
```Shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

### Install the powerlevel9k theme
```Shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

### Set theme inside Zsh config inside ```**~/.zshrc**```
```Shell
ZSH_THEME="powerlevel10k/powerlevel10k"
```

### To access the configuration wizard
```Shell
p10k configure
```