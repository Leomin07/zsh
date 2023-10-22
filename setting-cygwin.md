### 1. Recommended checked packages: lynx, wget, tar, git, vim, zsh
### 2. Install apt-cyg
```
wget -P /bin/ rawgit.com/transcode-open/apt-cyg/master/apt-cyg
chmod +x /bin/apt-cyg
```

### 3. Install Oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### 4. Add cygwin to Windows Terminal
- Command-line
```
C:\cygwin64\bin\bash.exe --login
```
- Icon
```
C:\cygwin64\Cygwin.ico
```
- Name
```
Cygwin Bash
``` 
- Tab title
```
Cygwin shell
```
