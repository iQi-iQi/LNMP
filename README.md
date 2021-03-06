LNMP1.1
====
LNMPはLinux Shellで作成され、簡単にLNMP環境(Linux+Nginx+MySQL/MariaDB+PHP+phpMyAdmin)を作成するツールです。
Linux(CentOS/RadHat、Debian/Ubuntu)
LNMP公式サイト：http://lnmp.jp.ai/

--------------------------------------------------------------------------------

インストール
————
※詳細について、公式サイト(http://lnmp.jp.ai/)にご確認ください。

screen -S lnmp
CentOSの場合：wget -c http://soft.jp.ai/lnmp/lnmp1.1.tar.gz && tar zxf lnmp1.1-full.tar.gz && cd lnmp1.1-full && ./centos.sh
Debianの場合：wget -c http://soft.jp.ai/lnmp/lnmp1.1.tar.gz && tar zxf lnmp1.1-full.tar.gz && cd lnmp1.1-full && ./debian.sh
Ubuntuの場合：wget -c http://soft.jp.ai/lnmp/lnmp1.1.tar.gz && tar zxf lnmp1.1-full.tar.gz && cd lnmp1.1-full && ./ubuntu.sh

途中接続切れた場合：screen -r lnmp

LNMPA(Apacheを追加してインストールしたい場合)：
./apache.sh

Option
————————

FTP：
./pureftpd.sh (pureftpをインストールする場合、「http://yourIP/ftp/」で管理する)
./proftpd.sh  (proftpをインストールする場合、「/root/proftpd_vhost.sh」で管理する)

Upgrade：
./upgrade_nginx.sh Nginxのupgrade
./upgrade_php.sh   PHPのupgrade
./upgrade_mysql.sh MySQLのupgrade（データをバックアップするうえでご利用ください）
./upgrade_mysql2mariadb.sh MySQLからMariadbにアップデート（データをバックアップするうえでご利用ください
./upgrade_mariadb.sh Mariadbのupgrade（データをバックアップするうえでご利用ください）
./upgrade_lnmpa_php.sh LNMPA-PHPのupgrade

Cache：
./xcache.sh http://yourIP/xcache/で管理、ユーザ名前：admin
./redis.sh
./memcached.sh
./opcache.sh http://yourIP/ocp.phpで管理
./eaccelerator.sh

Image：
./imageMagick.sh imageMagick：/usr/local/imagemagick/bin/

decode：
./ionCube.sh

Other：
./reset_mysql_root_password.sh MySQL/MariaDBのrootパスワードをリセットする
./check502.sh  check php-fpm 502 error
./cut_nginx_logs.sh nginx log cut tools
./remove_disable_function.sh remove disabled functions
./uninstall.sh unstall lnmp

Status command:
————————

LNMP：/root/lnmp {start|stop|reload|restart|kill|status}
LNMPA：/root/lnmpa {start|stop|reload|restart|kill|status}
Nginx：/etc/init.d/nginx {start|stop|reload|restart}
MySQL：/etc/init.d/mysql {start|stop|restart|reload|force-reload|status}
MariaDB：/etc/init.d/mariadb {start|stop|restart|reload|force-reload|status}
PHP-FPM：/etc/init.d/php-fpm {start|stop|quit|restart|reload|logrotate}
PureFTPd：/etc/init.d/pureftpd {start|stop|restart|kill|status}
Apache：/etc/init.d/httpd {start|stop|restart|graceful|graceful-stop|configtest|status}

vhost：/root/vhost.sh
phpinfo：http://yourIP/phpinfo.php
PHPMyAdmin：http://yourIP/phpmyadmin/
PHP：http://yourIP/p.php
PureFtp：http://yourIP/ftp/
Xcache：http://yourIP/xcache/
Zend Opcache：http://yourIP/ocp.php

LNMP File Location
————————————————
Nginx：/usr/local/nginx/
MySQL：/usr/local/mysql/
MariaDB：/usr/local/mariadb/
PHP：/usr/local/php/
PHPMyAdmin：/home/wwwroot/default/phpmyadmin/
site default location：/home/wwwroot/default/
Nginx Log：/home/wwwlogs/

LNMP Config File Location
————————————————
Nginx：/usr/local/nginx/conf/nginx.conf
MySQL/MariaDB：/etc/my.cnf
PHP：/usr/local/php/etc/php.ini
PureFtpd：/usr/local/pureftpd/pure-ftpd.conf
PureFtpd MySQL：/usr/local/pureftpd/pureftpd-mysql.conf
Apache：/usr/local/apache/conf/httpd.conf


support
————————
公式サイト：http://code.jp.ai/wiki/lnmp
