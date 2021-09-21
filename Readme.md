# 🐳 Docker + PHP 7.4 + MySQL + PostgreSQL + Nginx + Symfony 5

## Description

This is a complete stack for running Symfony 5 into Docker containers using docker-compose tool.

It is composed by 3 containers:

- `nginx`, acting as the webserver.
- `php`, the PHP-FPM container with the 7.4 PHPversion.
- `mysql` which is the MySQL database container with a **MySQL 8.0** image.
- `postgresql` which is the MySQL database container with a **PostgreSQL 13-alpine** image.

## Installation

1. 😀 Clone this rep.

2. Run `docker-compose up -d`

3. The 3 containers are deployed: 

```
Creating mysql    ... done
Creating nginx   ... done
Creating php ... done
Creating postgresql ... done
```

4. Use this value for the DATABASE_URL environment variable of Symfony:

```
DATABASE_URL=mysql://app_user:helloworld@db:3306/app_db?serverVersion=5.7 (MySQL)
DATABASE_URL=postgresql://127.0.0.1:5432/db?serverVersion=13&charset=utf8 (PostgreSQL)
```

You could change the name, user and password of the database in the `env` file at the root of the project.
