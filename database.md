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
sudo apt install mongodb
```
status mongo
```
sudo systemctl status mongodb
```
```
mongo
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
