## Installed Mysql on ubuntu-22.04, not error
```
sudo apt-get remove --purge mysql-server mysql-client mysql-common
sudo apt-get autoremove
sudo apt-get autoclean
sudo rm -rf /etc/mysql /var/lib/mysql
sudo apt-get update
sudo apt-get install -y mysql-server
sudo systemctl start mysql
```
