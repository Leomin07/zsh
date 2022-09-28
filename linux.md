# 1. Xoa 1 line in nano editor
```
control + K
```
# 2. Add thêm các ssh key khác
```
nano ~/.ssh/authorized_keys
```
1. Install Curl
```
sudo apt install curl
```

2. Install node@14
```
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
```
```
sudo apt-get install -y nodejs
```
3. Install mysql
```
sudo apt install mysql-server
```
# 3. Swap ram trong linux/ubuntu
##### 1. Creating a Swap File
```
sudo fallocate -l 2G /swapfile
```
##### 2. Set up Swap File Permissions
```
sudo chmod 600 /swapfile
```
##### 3. Set up a Swap Space
```
sudo mkswap /swapfile
```
```
Output
Setting up swapspace version 1, size = 1024 MiB (1073737728 bytes)
no label, UUID=f59595fb-754b-47ae-af6b-8dd6e98654d8
```
##### 4. Enable Swap Space
```
sudo swapon /swapfile
```
##### 5. Verify that the swap is available by typing:
```
sudo swapon --show
```

```
Output
NAME      TYPE  SIZE USED PRIO
/swapfile file 1024M   0B   -2
```
##### 6.You can check the output of the free utility again.
```
free -h
```

```
Output
               total        used       free        shared      buff/cache  available
Mem:           581M         275M        62M        103M        243M        110M
Swap:          1.0G          0B        1.0G
```

[Link tutorial](https://www.cloudbooklet.com/how-to-add-swap-space-on-ubuntu-20-04/)







