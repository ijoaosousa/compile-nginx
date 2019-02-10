INSTALAR ATUALIZAÇÕES DO SISTEMA CENTOS 7

sudo curl -o install-updates -L https://raw.githubusercontent.com/ijoaosousa/install-web-server/master/install-updates

sh install-updates

INSTALAR O NGINX COM OS MODULOS

sudo curl -o install-nginx -L https://raw.githubusercontent.com/ijoaosousa/install-web-server/master/install-nginx

sh install-nginx

INSTALAR O PHP-FPM 7.2.15

sudo curl -o install-php -L https://raw.githubusercontent.com/ijoaosousa/install-web-server/master/install-php

sh install-php

INSTALAR PHPMYADMIN E ADMINER

cd /var/www/html

sudo wget https://files.phpmyadmin.net/phpMyAdmin/4.8.5/phpMyAdmin-4.8.5-all-languages.zip

unzip phpMyAdmin-4.8.5-all-languages.zip

sudo wget https://github.com/vrana/adminer/releases/download/v4.7.1/adminer-4.7.1.php


INSTALAR O PERCONA SERVER 5.7

sudo rm -rf /etc/my.cnf.d

sudo rm -rf /etc/my.cnf

sudo yum install https://repo.percona.com/yum/percona-release-latest.noarch.rpm

sudod yum install Percona-Server-server-57

sudo service mysql start

sudo grep "temporary password" /var/log/mysqld.log

ALTER USER root@localhost IDENTIFIED BY 'novasenha';
