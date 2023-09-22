# Postgres and webmin dockerized

The purpose is to let you run postgres and webmin quickly container with minimal config

## Prerequisites
- Docker engine already installed 

## Steps
- Clone repository
``` 
git clone https://github.com/fenny-mdg/postgres-webmin.git
 ```
- Navigate to directory and copy .env.example to .env
```
cd postgres-webmin && cp .env.example .env
```
- Enter the value of each variable inside .env file 
```
# For security reasons, it is recommended to use a strong password
PG_PASSWORD=strongPassword
# The directory where the data will be stored
PG_DATA=
# Port to access the database from the host
PG_PORT=9010
# Port to access adminer UI from the host
ADMINER_PORT=6050
```
- Run docker compose to start containers 
```
docker compose --env-file .env up -d
```