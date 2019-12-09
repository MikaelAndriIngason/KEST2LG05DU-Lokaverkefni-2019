# KEST2LG05DU-Lokaverkefni-2019

**Overview**
1. [Static IP address](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#1---static-ip-address)
2. [Hostname and domain name](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#2---hostname-and-domain-name)
3. [DHCP protocol](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#3---dhcp-protocol) 
4. [DNS server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#4---dns-server) 
5. [Groups and users](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#5---groups-and-users) 
6. [Samba share folder](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#6---samba-share-folder) 
7. [SSH protocol](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#7---ssh-protocol) 
8. [apache2 web server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#8---apache2-web-server) 
9. [MYSQL server and phpmyadmin web interface](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#9---mysql-server-and-phpmyadmin-web-interface) 
10. [Postfix mail server](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#10---postfix-mail-server) 
11. [PurFTPd and Quota](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#11---purftpd-and-quota) 
12. [SquirreMail](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#12---squirremail) 
13. [ISPConfig-3](https://github.com/MikaelAndriIngason/KEST2LG05DU-Lokaverkefni-2019/blob/master/README.md#13---ispconfig-3) 

> https://www.howtoforge.com/tutorial/perfect-server-ubuntu-18.04-with-apache-php-myqsl-pureftpd-bind-postfix-doveot-and-ispconfig/ bara að geyma.

---
## 1 - Static IP address

**Static IP**
> $ sudo nano /etc/netplan/01-network-manager-all.yaml
---
![Static IP](/screenshots/staticip.png)

---
## 2 - Hostname and domain name

**Hostname**
> $ sudo nano /etc/hosts
---
![Hostname](/screenshots/hostname.png)

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


---
## 7 - SSH protocol

* sudo nano /etc/ssh/ssh_config
* sudo service ssh status

https://vitux.com/how-to-remotely-manage-a-ubuntu-server-with-ssh/

> virkar ekki á client - og þarf að setja group permissions fyrir IT og Management.

---
## 8 - apache2 web server

**Apache2 web server and demo website**\n
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

> Búinn að installa, get ekki komist inn á phpmyadmin á netinu, þarf að gera accounts fyrir IT og Management.

---
## 10 - Postfix mail server

https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-postfix-on-ubuntu-18-04

> Bara búið að installa.

---
## 11 - PurFTPd and Quota

**Pure-FTPd**
> $ sudo systemctl status pure-ftpd
---
![Pure-ftpd](/screenshots/pure-ftpd.png)

https://www.digitalocean.com/community/tutorials/how-to-set-filesystem-quotas-on-ubuntu-18-04

> Bara búið að installa bæði Pure-FTPd og Quota, þarf að enable-a Quota.

---
## 12 - SquirreMail

> Þarf að laga postfix til að gera þetta.

---
## 13 - ISPConfig-3
