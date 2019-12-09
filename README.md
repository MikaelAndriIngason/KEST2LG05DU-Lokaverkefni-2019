# KEST2LG05DU Lokaverkefni 2019

**Overview**
1. [Static IP address](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#1---static-ip-address)
2. [Hostname and domain name](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#2---hostname-and-domain-name)
3. [DHCP protocol](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#3---dhcp-protocol) 
4. [DNS server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#4---dns-server) 
5. [Groups and users](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#5---groups-and-users) 
6. [Samba share folder](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#6---samba-share-folder) 
7. [SSH protocol](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#7---ssh-protocol) 
8. [apache2 web server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#8---apache2-web-server) 
9. [MYSQL and phpmyadmin](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#9---mysql-server-and-phpmyadmin-web-interface) 
10. [Postfix mail server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#10---postfix-mail-server) 
11. [Pure-FTPd and Quota](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#11---purftpd-and-quota) 
12. [SquirrelMail](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#12---squirrelmail) 
13. [ISPConfig-3](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#13---ispconfig-3) 

> https://www.howtoforge.com/tutorial/perfect-server-ubuntu-18.04-with-apache-php-myqsl-pureftpd-bind-postfix-doveot-and-ispconfig/ bara að geyma.

---
## 1 - Static IP address

**Static IP Configuration**
> $ sudo nano /etc/netplan/01-network-manager-all.yaml
---
![Static IP](/screenshots/staticip.png)

---
## 2 - Hostname and domain name

**Host and domain name configuration**
> $ sudo nano /etc/hosts
---
![Hostname](/screenshots/hostdomainname.png)

---
## 3 - DHCP protocol

**DHCP Configuration**
> $ sudo nano /etc/dhcp/dhcpd.conf
---
![DHCP conf](/screenshots/dhcp1.png)

**DHCP Status**
> $ sudo systemctl status isc-dhcp-server.service
---
![DHCP Status](/screenshots/dhcp2.png)

**DHCP Client IP**
> $ ip add sh
---
![DHCP clientip](/screenshots/dhcp3.png)

---
## 4 - DNS server

**DNS Configuration**
> $ sudo nano /etc/netplan/01-network-manager-all.yaml
---
![DNS conf](/screenshots/dns.png)

---
## 5 - Groups and users

> $ sudo adduser [name]
  
> $ sudo addgroup [name]


**Users**
> $ ls /home/
---
![Users](/screenshots/users.png)

**Groups**
> $ cat /etc/group
---
![Groups](/screenshots/groups.png)

---
## 6 - Samba share folder

**Samba Status**
> $ sudo systemctl status nmbd
---
![samba status](/screenshots/samba1.png)

Samba configuration
> $ sudo nano /etc/samba/smb.conf
---
![samba conf](/screenshots/samba2.png)

New samba user:
> $ sudo smbpasswd -a [username] 

---
## 7 - SSH protocol

**SSH Status**
> $ sudo service ssh status
---
![ssh status](/screenshots/ssh1.png)

SSH configuration
> $ sudo nano /etc/ssh/ssh_config

To connect to SSH from client:
> $ ssh -l [username] 192.168.100.1
---
![ssh demo](/screenshots/ssh2.png)

---
## 8 - apache2 web server

**Apache2 web server and demo website**  

To change index file of the website:
> $ sudo nano /var/www/html/index.html
---
![apache2 demo](/screenshots/apache2.png)

**SSL**
> https://linuxpropaganda.wordpress.com/2018/07/06/enable-ssl-for-apache2-in-ubuntu-server-18-04/2/
---
![apache2 ssl](/screenshots/apache2_ssl.png)

---
## 9 - MYSQL server and phpmyadmin web interface

**MYSQL**  
Installed, to log in:
> $ mysql -u root -p
---
![mysql](/screenshots/mysql.png)

**phpMyAdmin**  
Installed, but does not show up in http://mikael.local/phpmyadmin or http://192.168.100.1/phpmyadmin

---
## 10 - Postfix mail server

**Postfix Status**
> $ sudo systemctl status postfix
---
![postfix status](/screenshots/postfix.png)

Assign emails:
> $ sudo nano /etc/postfix/virtual
---
![postfix emails](/screenshots/postfixemails.png)

---
## 11 - Pure-FTPd and Quota

**Pure-FTPd**
> $ sudo systemctl status pure-ftpd
---
![Pure-ftpd](/screenshots/pure-ftpd.png)

**Quota**  
To change user quota:
> $ sudo edquota -u [name]

To change group quota:
> $ sudo edquota -g [name]

---
## 12 - SquirrelMail

**SquirrelMail configuration**
> $ sudo nano /var/www/html/mail/config/config.php

> Þarf að laga postfix til að gera þetta.

---
## 13 - ISPConfig-3
