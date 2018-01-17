# 套件依賴
* build-essential
* bison
* flex
* libjpeg-dev
* libpng-dev
* libXpm-dev
* libcurl4-openssl-dev
* libmhash-dev
* libmcrypt-dev
* libreadline-dev
* libedit-dev
* libtidy-dev
* libssl-dev
* systemtap-sdt-dev - dtrace
* libzip-dev
* libxml2-dev
* libicu-dev
* libxslt-dev
* libpcre3-dev
* automake
* autoconf
* libmysqlclient-dev - php5.2
* libsodium-dev - php7.2
* argon2 https://github.com/P-H-C/phc-winner-argon2

```
# apt install build-essential bison flex libjpeg-dev libpng-dev libXpm-dev libcurl4-openssl-dev libmhash-dev libmcrypt-dev libmysqlclient-dev libreadline-dev libedit-dev libtidy-dev libssl-dev systemtap-sdt-dev libzip-dev libxml2-dev libicu-dev libxslt-dev libpcre3-dev libsodium-dev automake autoconf
```

# 編譯 argon2

```
# apt install git
# cd /usr/src
# git clone https://github.com/P-H-C/phc-winner-argon2
# cd phc-winner-argon2
# git checkout 20171227
# make install
```

#安裝 apach2

```
# apt install apache2
```

#下載 Source Code

* php 7.2.1 - http://php.net/downloads.php
* php 5.6.33 - http://php.net/downloads.php
* php 5.2.17 - http://php.net/releases/

# 下載 PHP 5.2 Patch

* PHP-FPM - https://php-fpm.org/downloads/
* libxml2 - https://mail.gnome.org/archives/xml/2012-August/txtbgxGXAvz4N.txt
* openssl-1.0.0 sslv2 - https://github.com/centos-bz/ezhttp/blob/master/conf/debian_patches_disable_SSLv2_for_openssl_1_0_0.patch
* fastcgi apache patch - patch/php-5.2.17-fcgi-script-filename.diff

# 打 PHP 5.2 補丁

```
# cd php-5.2.17
# zcat ../php-5.2.17-fpm-0.5.14.diff.gz|patch -p1
# patch -p0 < ../txtbgxGXAvz4N.txt
# patch -p1 < ../debian_patches_disable_SSLv2_for_openssl_1_0_0.patch
# patch -p1 < ../php-5.2.17-fcgi-script-filename.diff
```

# 編譯 PHP

```
# cd php-xxx
# ./setup-xxx
# make clean
# make install
```

