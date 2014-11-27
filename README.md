docker-oracle-xe-11g
============================

## Oracle XE - Dockerfile

This repository contains a **Dockerfile** to create a docker container with Oracle Express Edition 11g Release 2

This **Dockerfile** has been published as a [trusted build](https://index.docker.io/u/alexeiled/docker-oracle-xe-11g/) to the public [Docker Registry](https://index.docker.io/).


### How-To: Install and Use


```
docker pull alexeiled/docker-oracle-xe-11g
```

Run with 22, 1521 and 8080 ports opened:
```
docker run -d -p 49160:22 -p 49161:1521 -p 49162:8080 alexeiled/docker-oracle-xe-11g
```

Connect database with following setting:
```
hostname: localhost
port: 49161
sid: xe
username: system
password: oracle
```

Password for SYS
```
oracle
```

Connect to Oracle Application Express web management console with following settings:
```
url: http://localhost:49162/apex
workspace: INTERNAL
user: ADMIN
password: oracle
```

Login by SSH
```
ssh root@localhost -p 49160
password: admin
```
