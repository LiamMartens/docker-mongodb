# MongoDB
This image is built on `Alpine`

## Build arguments
* `USER`: The non-root user to be used in the container (defaults to `mongo`)
* Any build arguments from the `Alpine` base image [liammartens/alpine](https://hub.docker.com/r/liammartens/alpine/)

## Directories
* `/etc/mongod`: For mongod configuration file(s) (default file is present)
* `/data`: For persistent data

## Logging
`mongod` starts with the logpath pointing to `/prof/self/fd/2`, which is `stdout` for docker.

## Environment
You can control several options for MongoDB  
* `MONGODB_PORT`: Defines which port to bind the server to (defaults to `27017`)
* `MONGODB_ADMIN_USER`: Defines what username to use as admin user (deafults to `admin`)
* `MONGODB_ADMIN_PASS`: Defines the admin password to use (randomly generated if none given, passed to `stdout`)
* `MONGODB_NAME`: The default database name, if given a `readWrite` user is also created (optional)
* `MONGODB_USER`: The `readWrite` username for the default database (defaults to the database name)
* `MONGODB_PASS`: The password for the database user (randomly generated if none given, passed to `stdout`)