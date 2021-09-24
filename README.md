1, install zsh

```
sudo apt-get install zsh
```

2, install oh my zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

- Add the plugin to the list of plugins for Oh My Zsh to load (inside ~/.zshrc):

3, zsh-autosuggestions

```
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
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
4. Default bash

```
chsh -s $(which zsh)
```

5, Create file 
```
touch 'name'
```
6, Open file
```
nano 'name'
```

Done
