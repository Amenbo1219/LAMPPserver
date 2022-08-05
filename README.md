# LAMPPserver
This is LAMPPserver on Docker-compose
nginx,phpmyadmin,Php,Python
# Howto
Unpack on LocalHostServer
Use ports 80,88,8088 
Set htmlScript on ./html
Set phpScropt on ./html/site/list
* localhost:80 HTML&CSS&JSserver
* localhost:88 Phpsupportserver
* localhost:8088 phpmyadminController

# Specs
Making docker images on Ubuntu-Desktop22.04 but maybe used on WSL and MacOS

* OS:Ubuntu22.04orMacOS Catalina orWindows10 18H2 on WSL
* CPU:2Cores on Intelx86orAMD64Prosessor (Not support Arm64Chips)
* Memory:4GB(8GB)
* Storage:256GB(10GB FreeSpace)
*  Special:
    Installed Docker and Docker-compose and Browser(GoogleChorme)
# Instration
Git clone this project
```sh
$ git clone  https://github.com/Amenbo1219/LAMPPserver.git
```
CangeDirectory
```sh
$ cd LAMPPserver/
```
Docker & Docker-compose check
```sh
$ Docker -v 
Docker version 20.10.12, build e91ed57
$ Docker-compose -v
docker-compose version 1.29.2, build 5becea4c
```
Docker-compose up 
```sh
$ docker-compose up -d
Creating network "lamppserver_default" with the default driver
・・・
Creating lamppserver_phpmyadmin_1 ... done
```
Check Docker logs 
```sh
$ Docker-compose logs
・・・
db_1          | Version: '5.7.39'  socket: '/var/run/mysqld/mysqld.sock'  port: 3306  MySQL Community Server (GPL)
```


Copyright Amembo1219/Tokyo Univercity of Technology/AdvancedCreators