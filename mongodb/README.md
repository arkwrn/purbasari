# MongoDB in Docker

## Usage (start server)

### Single server

```
// non detach mode
docker-compose up
```
or
```
// detach mode
docker-compose up -d
```

### Server with replicaset

```
// non detach mode
docker-compose up -f docker-compose-replicaset copy.yml
```
or
```
// detach mode
docker-compose up -d
```

It will spin the MongoDB latest version (currently 4.x.x version), expose port to host at 27017.

## Usage (stop server)

To shutdown database without remove the container.

```
docker-compose stop
```

To shutdown database and remove the container.
```
docker-compose down
```

Every data that stored on the docker will be saved under `mongo_data` volume which is saved on your local, please change the path on compose file to fit your own local path location.