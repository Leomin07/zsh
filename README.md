1, install zsh

```
sudo apt-get install zsh -y
```

2, install oh my zsh

```
sudo curl -L http://install.ohmyz.sh | sh
```

- Add the plugin to the list of plugins for Oh My Zsh to load (inside ~/.zshrc):

3, zsh-autosuggestions

```
git clone git://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
```

```
nano .zshrc
```
```
plugins=(git
zsh-autosuggestions zsh-syntax-highlighting
)
```
```
source .zshrc
```
4, zsh-syntax-highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
5, powerlevel10k
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
```
ZSH_THEME="powerlevel10k/powerlevel10k"
```
6, Default bash

```
chsh -s $(which zsh)
```

7, Create file 
```
touch 'name'
```
8, Open file
```
nano 'name'
```
9, update
```
sudo apt update
```
10, theme
```
awesomepanda
```
11, font
```
https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup
```
Done
