1, install zsh

```
sudo apt-get install zsh -y
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
OR
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
```
nano .zshrc
```
```
plugins=(
zsh-autosuggestions
)
```
```
source .zshrc
```

4. Đặt zsh làm mặc định

```
chsh -s $(which zsh)
```

Done
