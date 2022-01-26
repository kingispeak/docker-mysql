# Docker + MySQL

Run a MySQL server locally via Docker in MacOS.

## Prerequisites

Before you get started, you need to make sure that you have Docker and Docker Compose installed.

You can follow the steps here on how to install Docker:

> [Installing Docker](https://www.docker.com/get-started)

## Install

First, start by cloning the repository:

```
git clone https://github.com/kingispeak/docker-mysql8.git
```

After that you can access the directory:

```
cd docker-mysql8
```

Let's start by first running the db container:

```
docker-compose up -d db
```

Build the images:

```
docker-compose build
```

Finally, start all of the services:

```
docker-compose up -d
```


## Use

Connect via mysql CLI tool

> To connect to the MySQL server from your terminal, you need to have a MySQL client installed.

```
brew install mysql-client
```

Connect via docker in container

```
docker exec -it 6e96aa3334ff44f2517682978fa93ead568d7f2a9ef5e1208ba7e3b9bfbffa37 /bin/sh
```

Connect mysql server

```
mysql -h localhost --protocol=TCP -u root -p
```


Show databases

```sql
show databases;
```

You would be able to see that.

```sql
--------------------+
 Databases
--------------------+
 information_schema
 mysql
 performance_schema
 sys
 testdb
--------------------+
5 rows in set (0.01 sec)
```

