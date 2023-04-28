### 1. Download package [here](./zsh-5.9-2-x86_64.pkg.tar.zst)

### 2. Extract to:

```
C:\Program Files\Git
```

### 3. Test it and config zsh:

- Open git bash and type:

```
zsh
```

- type `0` not config setting.

### 4. Installing oh-my-zsh, execute the following cmd on git bash

- Install oh-my-zsh

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### 5. Configuring zsh as default shell

```
# Launch Zsh
if [ -t 1 ]; then
exec zsh
fi
```

### 6. Install plugins

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

### 7. Optional steps

- Install theme

```
curl -fsSL https://raw.githubusercontent.com/oskarkrawczyk/honukai-iterm/master/honukai.zsh-theme -o ~/.oh-my-zsh/custom/themes/honukai.zsh-theme
```

- Set it

```
sed -i 's/ZSH_THEME="robbyrussell"/ZSH_THEME="honukai"/g' ~/.zshrc
```

### 8. Fixing Mangled Output

Windows can mangle some UTF-8 encoded text, causing unexpected characters to be displayed in your terminal (more info in this Stack Overflow answer). To fix this, add the following to your ~/.bashrc file, ideally before code that sets your shell as Zsh:

```
/c/Windows/System32/chcp.com 65001 > /dev/null 2>&1

```

### 9. Config them agnoster [here](./install-theme-custom-agnoster.md)

### 10. Set zsh default

```
chsh -s $(which zsh)
```
