## INSTALL APACHE
```sudo yum -y update
sudo yum -y upgrade
sudo yum -y install httpd
sudo systemctl start httpd.service
sudo systemctl status httpd
sudo systemctl enable httpd
```

## OPEN 80 PORT
```sudo firewall-cmd --list-all
sudo firewall-cmd --add-service=http --permanent
sudo firewall-cmd --reload
```

## INSTALL mysql (mariadb)

```sudo yum -y install mariadb-server mariadb
sudo systemctl start mariadb
sudo mysql_secure_installation
sudo systemctl enable mariadb.service
```

## INSTALL PHP
```sudo yum -y install php php-mysql
sudo systemctl restart httpd.service
sudo vim /var/www/html/info.php 			
	"<?php phpinfo(); ?>"
sudo systemctl restart httpd.service
```
