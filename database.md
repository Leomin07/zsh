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

