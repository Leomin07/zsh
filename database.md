## Mysql
### 1. Change password root
```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'newPassword';
```
Create new user
```
CREATE USER 'user'@'hostname';
```
Access db
```
GRANT ALL PRIVILEGES ON dbTest.* To 'user'@'hostname' IDENTIFIED BY 'password';
```
fix change password root
```
SET GLOBAL validate_password.LENGTH = 4;
SET GLOBAL validate_password.policy = 0;
SET GLOBAL validate_password.mixed_case_count = 0;
SET GLOBAL validate_password.number_count = 0;
SET GLOBAL validate_password.special_char_count = 0;
SET GLOBAL validate_password.check_user_name = 0;
ALTER USER 'user'@'localhost' IDENTIFIED BY 'pass';
FLUSH PRIVILEGES;
```
## MongoDB
### 1. Install mongodb
```
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
```
```
apt-key list
```
```
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```
```
sudo apt update
```
```
sudo apt install mongodb-org
```
```
sudo systemctl start mongod.service
```
```
sudo systemctl status mongod
```
```
sudo systemctl enable mongod
```
```
mongo --eval 'db.runCommand({ connectionStatus: 1 })'
```
```
sudo systemctl status mongod
```
### Redis
### 1. Install Redis
```
sudo add-apt-repository ppa:chris-lea/redis-server
```

```
sudo apt-get update
```

```
sudo apt-get install redis-server
```
### 2. Start  redis

```
sudo service redis-server start
```
### 3. Rename namespace pm2
```
pm2 restart "idPm2" --name "newName"
```
