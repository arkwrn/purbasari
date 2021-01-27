# MongoDB in Docker

## Usage (start server)

```
// non detach mode
docker-compose up
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

## MongoDB credential (for database `admin`)

- Username: root
- Password: <YOUR_ROOT_PASSWORD>

## How to connect to MongoDB

### Via mongo Shell

```
mongo admin -u root -p <YOUR_ROOT_PASSWORD>
```

It will connect to localhost port 27017.

Note that `mongo` command should be installed on the computer. 
On Linux this should be install `mongodb-org-shell` only. 
Refer to this for more detail https://docs.mongodb.com/manual/installation/

### Mongo command

Show databases:
```
show dbs
```

Create new non-existant database:
```
use mydatabase
```

Show collections:
```
show collections
```

Show contents of a collection:
```
db.your_collection_name.find()
```

Save a data to a collection:
```
db.your_collection_name.save({"name":"Arie Kurniawan"})
```

Show database version:
```
db.version()
```