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
plugins=(
zsh-autosuggestions zsh-syntax-highlighting
)
```
```
source .zshrc
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
