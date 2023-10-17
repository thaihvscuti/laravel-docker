# Install and Set Up Laravel with Docker Compose

Setting up Laravel in the local environment with Docker using the LEMP stack that includes: Nginx, MySQL, PHP, and phpMyAdmin.

## Why use Docker for Development

- [x] Consistent development environment for the entire team.
- [x] You don't need to install a bunch of language environments on your system.
- [x] You can use different versions of the same programming language.
- [x] Deployment is easy

## How to Install and Run the Project

1. ```docker-compose build```
2. ```docker compose up -d```
3. ```cd src```
4. Copy ```.env.example``` to ```.env```
5. ``` docker-compose exec app composer install ```
7. ```docker-compose run --rm npm install```
8. ```docker-compose run --rm npm run dev```
9. ```docker-compose run --rm npm run build```
10. ```docker-compose exec app php artisan key:generate```
11. You can see the project on ```127.0.0.1:8080```

## How to use MySQL as a database

1. Uncomment the MySQL configuration inside the ```docker-compose.yml``` including: ```db``` and ```phpMyAdmin```
2. Copy ```.env.example``` to ```.env```
3. Change ```DB_CONNECTION``` to ```mysql```
4. Change ```DB_PORT``` to ```3306```
5. Open the ```phpMyAdmin``` on ```127.0.0.1:3400```

## How to use PostgreSQL as a database

1. Uncomment the PostgreSQL configuration inside the ```docker-compose.yml``` including: ```db``` and ```pgamdin```
2. Copy ```.env.example``` to ```.env```
3. Change ```DB_CONNECTION``` to ```pgsql```
4. Change ```DB_PORT``` to ```5432```
5. Open the ```pgAdmin``` on ```127.0.0.1:5050```

## How to run Laravel Commands with Docker Compose

1. ```cd src```
2. ```docker-compose exec app php artisan {your command}```
