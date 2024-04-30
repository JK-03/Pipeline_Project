---
title : "Backend"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.3.5.2 </b> "
---

#### Project workflow
1. Tools
2. Edit & configure files
3. Install & configure Database
4. Build
5. Run
6. Check status

#### Configuration
Source: shoeshop-ecommerce.zip

User: shoeshop

Project folder: /projects/shoeshop
1. Requires tools: Maven, Java, Mariadb

````
apt install openjdk-17-jdk openjdk-17-jre
apt install maven
java -version
mnv -v
````

````
apt install mariadb-server
netstart -tlpun
````
2. Configure

Mariadb

````
systemctl stop mariadb
````
nano /etc/mysql/mariadb.conf.d/50-server.conf
````
bin-address = 0.0.0.0
````
````
systemctl restart mariadb
````
mysq -u root
````
show databases;
create database shoeshop;
create user 'shoeshop'@%'identified by 'shoeshop';
grant all privileges on shoeshop.* to 'shoeshop'@'%';
flush privileges;
exit
````

mysq -h 192.168.33.110 -P 3306 -u shoeshop
````
show databases;
use shoeshop;
show tables;
source /projects/shoeshop/shoeshopdb.sql
show tables;
exit
````
vi /src/main/resources/application.properties
````
spring.datasource.url=jdbc:mysql://192.168.33.110:3306/shoeshop
spring.datasource.username=shoeshop
spring.datasource.password=shoeshop
````
mvn install -DskipTest=true

ls target/
````
java -jar target/shoe-ShoppingCart-0.0.1-SNAPSHOT.jar
````

````
nohup java -jar target/shoe-ShoppingCart-0.0.1-SNAPSHOT.jar 2>&1 &
````

tail -f nohup.out

3. Check: http://192.168.33.110:8080