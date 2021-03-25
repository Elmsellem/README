# PLESK & UBUNTU SOLUTIONS
## php not found on command line
export php path for current session
```bash
export PATH=/opt/plesk/php/7.3/bin/:$PATH
```
or add php path to /etc/profile (global initialization scripts)
```bash
sudo su
echo "PATH=/opt/plesk/php/7.3/bin/:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin" >> /etc/profile
# exit from root session
exit
```
## disable mysql strict mode
```bash
sudo su
echo 'sql_mode=""' >> /etc/mysql/my.cnf
service mariadb restart
# exit from root session
exit
```
