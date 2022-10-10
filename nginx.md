## DEPLOY BACKEND NodeJs.

1. Install Nginx.
```
sudo apt install nginx
```
2. Check firewall server (ubuntu).
- If inactive, skip
```
sudo ufw app list
```
```
Output
Available applications:
  Nginx Full
  Nginx HTTP
  Nginx HTTPS
  OpenSSH
```
```
sudo ufw allow 'Nginx HTTP'
```
```
sudo ufw status
```
3. Checking web server.
```
systemctl status nginx
```
```
● nginx.service - A high performance web server and a reverse proxy server
   Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
   Active: active (running) since Fri 2020-04-20 16:08:19 UTC; 3 days ago
     Docs: man:nginx(8)
 Main PID: 2369 (nginx)
    Tasks: 2 (limit: 1153)
   Memory: 3.5M
   CGroup: /system.slice/nginx.service
           ├─2369 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;
           └─2380 nginx: worker process
```
4. Setting server block.
```
sudo mkdir -p /var/www/your_domain/html
```
```
sudo chown -R $USER:$USER /var/www/your_domain/html
```
```
sudo chmod -R 755 /var/www/your_domain
```
```
sudo nano /var/www/your_domain/html/index.html
```
```
<html>
    <head>
        <title>Welcome to your_domain!</title>
    </head>
    <body>
        <h1>Success!  The your_domain server block is working!</h1>
    </body>
</html>
```
```
sudo nano /etc/nginx/sites-available/your_domain
```
```
sudo ln -s /etc/nginx/sites-available/your_domain /etc/nginx/sites-enabled/
```
```
sudo nano /etc/nginx/nginx.conf
```
```
...
http {
    ...
    server_names_hash_bucket_size 64;
    ...
}
...
```
```
sudo nginx -t
```
```
sudo systemctl restart nginx
```










