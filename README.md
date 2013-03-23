My personal configuration for nginx
===================================

This repo holds all the files and instructions needed to install nginx in a Debian box.

1.- Install all dependencies for nginx

```bash
aptitude install libpcre3 libpcre3-dev libpcrecpp0 libssl-dev zlib1g-dev build-essential
```

2.- Download the latest stable version

```bash
$ wget http://nginx.org/download/nginx-1.2.7.tar.gz
```

3.- Extract it

```bash
$ tar -xvzf nginx-1.2.7.tar.gz
```
4.- Install it

```bash
$ cd nginx-1.2.7
$ ./configure --pid-path=/var/run/nginx.pid --sbin-path=/usr/local/sbin --with-http_ssl_module
$ make
# make install
```

5.- Fetch nginx init-script file, copy into /etc/init.d and update rc.d

```bash
# wget https://github.com/satanas/nginx-conf/raw/master/nginx
# mv nginx /etc/init.d/
# chmod +x /etc/init.d/nginx
# insserv nginx
```

6.- Edit the nginx config file at your pleasure

7.- Enjoy!

Optional: Install PHP 5
=======================

1.- Install all dependencies for php

```bash
# aptitude install php5-cgi php5-mysql php5-curl php5-gd php5-idn php-pear php5-imagick php5-imap php5-json php5-mcrypt php5-memcache php5-mhash php5-ming php5-ps php5-pspell php5-recode php5-snmp php5-sqlite php5-tidy php5-xmlrpc php5-xsl
```

2.- Fetch php-fastcgi init-script file, copy into /etc/init.d and update rc.d

```bash
# wget https://github.com/satanas/nginx-conf/raw/master/php-fastcgi
# mv php-fastcgi /etc/init.d/
# chmod +x /etc/init.d/php-fastcgi
# insserv php-fastcgi
```



