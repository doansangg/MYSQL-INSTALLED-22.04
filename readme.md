## Camera Yoosee
```
rtsp://admin:Atnv@123@192.168.1.5:554/onvif1
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
