## Docker Seafile
```
docker run -d --name mariadb-seafile -e MYSQL_ROOT_PASSWORD=Sangdoan2009 -e MYSQL_DATABASE=seafile_db -e MYSQL_USER=seafile -e MYSQL_PASSWORD=123456 -p 3306:3306 -v /media/atnv/CSDL/db_seafile:/var/lib/mysql  mariadb:10.6


docker run -d --name minio -p 9000:9000 -p 9001:9001 -e "MINIO_ROOT_USER=admin" -e "MINIO_ROOT_PASSWORD=admin123" -v /media/atnv/MINIO/minio-data:/data quay.io/minio/minio server /data --console-address ":9001"

```

## Installed Mysql on ubuntu-22.04, not error
```
sudo apt-get remove --purge mysql-server mysql-client mysql-common
sudo apt-get autoremove
sudo apt-get autoclean
sudo rm -rf /etc/mysql /var/lib/mysql
sudo apt-get update
sudo apt-get install -y mysql-server
sudo systemctl start mysql
mysql -u root
ALTER USER 'root'@'localhost' IDENTIFIED BY mysql_native_password by/BY 'NewPasswordHere'
mysql -u root -p
```
## dev mysql
```
sudo apt install libmysqlclient-dev
```
## Export path
```
echo 'export MYSQL_CONFIG_PATH="/usr/bin/mysql_config"' >> ~/.bashrc
source ~/.bashrc
```
## Mout folder win into vmware 22.04
```
sudo nano /etc/fuse.conf
# open #user_allow_other
```
### run
```
/usr/bin/vmhgfs-fuse .host:/ /home/boring/Documents/data-out -o subtype=vmhgfs-fuse,allow_other
```
