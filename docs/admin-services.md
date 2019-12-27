# Start or Stop the Services

These commands you must know when you using the Seafile of Websoft9

### Seafile

```shell
sudo systemctl start awx-web
sudo systemctl stop awx-web
sudo systemctl restart awx-web
sudo systemctl status awx-web

sudo systemctl start awx-daphne
sudo systemctl stop awx-daphne
sudo systemctl restart awx-daphne
sudo systemctl status awx-daphne

sudo systemctl start awx-channels-worker 
sudo systemctl stop awx-channels-worker 
sudo systemctl restart awx-channels-worker 
sudo systemctl status awx-channels-worker 

sudo systemctl start awx-cbreceiver 
sudo systemctl stop awx-cbreceiver 
sudo systemctl restart awx-cbreceiver
sudo systemctl status awx-cbreceiver
```

### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

### PostgreSQL

```shell
# 11 is version number of PostgreSQL
sudo systemctl start postgresql-11
sudo systemctl stop postgresql-11
sudo systemctl restart postgresql-11
sudo systemctl status postgresql-11
```