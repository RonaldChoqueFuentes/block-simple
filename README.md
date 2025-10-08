# block-simple

- sample node js code use to create the docker compose
- https://blog.logrocket.com/crud-rest-api-node-js-express-postgresql/

##  common command to clean docker


```bash
docker system prune
docker images prune
docker stop $(docker ps -a -q)
docker rmi $(docker images -q)
docker volume rm :id
docker network rm :id

```
##  start docker componse

```bash
docker compose up

```

## endpoint

- http://localhost:8080/
- http://localhost:8080/users
- http://localhost:8080/users/:id

![alt text](screenshots/image.png)

## docker compose File
[docker compose File](docker-compose.yml)

## docker File
[node js docker file](app/Dockerfile)

## enviroment file variables for postgres
[postgres variables](.env)

## Api endpoints
[endpoint](app/queries.js)

##  Config File for postgrest
[SQL INIT](config/init.sql)
