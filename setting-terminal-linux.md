### 1. Install Zsh
```
sudo apt install zsh -y
```
### 2. Install Git
```
sudo apt install git-all -y
```
### 3. Install NodeJs version 14
- Install curl
```
sudo apt install curl
```
- Install NodeJS
```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
```
```
sudo apt-get install -y nodejs
```
### 4. Install plugins

- zsh-autosuggestions

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

- zsh-syntax-highlighting

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

- zsh-completions

```
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```

```
nano .zshrc
```

```
plugins=(
    zsh-autosuggestions zsh-completions zsh-syntax-highlighting git
)
```

```
source .zshrc
```
