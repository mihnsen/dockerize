# MySQL - dockerize

## Installation
```
docker pull mysql
mkdir -p $HOME/docker/volumes/mysql
docker run --name db-mysql -e MYSQL_ROOT_PASSWORD=docker -d -p 3306:3306 -v $HOME/docker/volumes/mysql:/var/lib/mysql mysql mysqld --default-authentication-plugin=mysql_native_password
```

## Access
```
docker exec -it db-mysql bash
// Inside docker container
mysql -u root -pdocker
show databases;
```

## Create database
```
create database <database_name> character set UTF8 collate utf8_general_ci;
```
