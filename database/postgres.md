# Postgres - dockerize
Follow the cross-platform-development

## Installation
```
docker pull postgres
mkdir -p $HOME/docker/volumes/postgres
docker run --name db-postgres -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v $HOME/docker/volumes/postgres:/var/lib/postgresql/data postgres
```


## Access it
```
docker exec -it db-postgres bash

// Then inside container
su postgres
psql
\l
```

## Create database
```
// Inside container postgres
CREATE DATABASE "db_name";
```
