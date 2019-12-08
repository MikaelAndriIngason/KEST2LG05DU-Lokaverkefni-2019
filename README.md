# KEST2LG05DU-Lokaverkefni-2019

https://www.howtoforge.com/tutorial/perfect-server-ubuntu-18.04-with-apache-php-myqsl-pureftpd-bind-postfix-doveot-and-ispconfig/

### 1 - Static IP address
![Static IP](/screenshots/staticip.png)

---
### 2 - Hostname and domain name


---
### 3 - DHCP protocol


---
### 4 - DNS server


---
### 5 - Groups and users

---
### 6 - Samba share folder


---
### 7 - SSH protocol

* sudo nano /etc/ssh/ssh_config
* sudo service ssh status

https://vitux.com/how-to-remotely-manage-a-ubuntu-server-with-ssh/

> virkar ekki á client - og þarf að setja group permissions fyrir IT og Management.

---
### 8 - apache2 web server

- [x] Installation: https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-18-04-quickstart
- [x] Demo site: sudo nano /var/www/html/index.html
- [x] SSL: https://linuxpropaganda.wordpress.com/2018/07/06/enable-ssl-for-apache2-in-ubuntu-server-18-04/2/

> Síðan kemur upp, demo-site og SSL er komið!

---
### 9 - MYSQL server and phpmyadmin web interface

> Búinn að installa, get ekki komist inn á phpmyadmin á netinu, þarf að gera accounts fyrir IT og Management.

---
### 10 - Postfix mail server

https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-on-ubuntu-18-04

> Bara búið að installa.

---
### 11 - PurFTPd and Quota

https://www.digitalocean.com/community/tutorials/how-to-set-filesystem-quotas-on-ubuntu-18-04

> Bara búið að installa bæði Pure-FTPd og Quota, þarf að enable-a Quota.

---
### 12 - SquirreMail

> Þarf að laga postfix til að gera þetta.

---
### 13 - ISPConfig-3
