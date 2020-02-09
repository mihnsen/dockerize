# MongoDB - dockerize
Follow the cross-platform-development

## Installation
```
docker pull mongo
mkdir -p $HOME/docker/volumes/mongo
docker run --rm --name db-mongo -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=docker -d -p 27017:27017 -v $HOME/docker/volumes/mongo:/data/db mongo
```


## Access it
```
docker exec -it db-mongo bash

// Then inside container
mongo
show dbs;
```

## Create database
```
// Inside container postgres
use "db_name";
```
