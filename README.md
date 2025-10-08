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



### 1. Título y Descripción

```markdown
# Block Simple

It is node js api  to list  update and create users 

**Curso:** Docker & Kubernetes - Clase 3
**Estudiante:** Ronald Choque Fuentes
**Fecha:** 10/08/2025
```

### 2. Stack Tecnológico

Lista las tecnologías usadas:

```markdown
## Stack Tecnológico

- **Backend:** Node.js + Express .
- **Base de datos:** PostgreSQL 15 c.
```

### 3. Arquitectura

Diagrama o descripción de la arquitectura:

```markdown
## Arquitectura

It use two services and nodeapp and db.  those are connected by common network.
the database use  a env file variables to set and  deploy the database.

Servicios:
- `app`: Puerto 8080, conectado a db 
- `db`: PostgreSQL, solo accesible desde app

```

Puedes incluir un diagrama ASCII o imagen.

### 4. Requisitos Previos

```markdown
## Requisitos

- Docker Desktop o Docker Engine
- Docker Compose
- Git
```

### 5. Instalación y Uso

Instrucciones paso a paso:

```markdown
## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/RonaldChoqueFuentes/block-simple.git
   cd block-simple
   ```

2. update default enviroment variables  :
 

3. Levantar servicios:
   ```bash
   docker compose up -d
   ```

4. Acceder a la aplicación:
   - API: http://localhost:8080
   - postgres database address: http://db:5432
```

### 6. Endpoints / Funcionalidad

Documenta cómo usar tu aplicación:

```markdown
## Endpoints

- `GET /` - default response
- `GET /users` - Listar items
- `GET /users/:id` - Listar items
- `POST /users/:id` - Crear item
