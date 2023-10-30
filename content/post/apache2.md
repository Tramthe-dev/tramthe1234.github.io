+++
title = 'Apache2'
date = 2023-10-30T09:31:14Z
+++

# How to install apache2 in termux version 0.118

````
pkg update -y

pkg install apache2 openssl-tools -y

````

# Now configure to server in html and type nano httpd.conf and type enter

```
cd ../usr/etc/apache2

nano httpd.conf

ssl

shmcb

http

httpd-ssl

httpd-vhosts

```
# Now save to httpd.conf

# In create floder to termux type mkdir ssl and type chmod 777 ssl and configure to httpd ssl & vhosts

```
mkdir ssl

chmod 777 ssl

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout $PREFIX/etc/apache2/ssl/cert.key -out $PREFIX/etc/apache2/ssl/cert.crt

cd extra

nano httpd-ssl.conf

nano httpd-vhosts.conf

redirect / http://127.0.0.1:8443 

```
# Now save to httpd-ssl-vhosts.conf and type apachectl
```
apachectl

```
# Open browser type termux-open-url http://127.0.0.1:8080

# This kill to apache2 server type killall apachectl

# Goodbye
# Thank for installation apache2 in termux
# Make by Technical bot
