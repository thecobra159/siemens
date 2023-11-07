# Siemens
Siemens Code Challenge API

- [Introdutcion](#introduction)
- [Update Submodules](#update-submodules)
- [Docker Compose](#docker-compose)
  - [Running Docker Compose](#running-docker-compose)
  - [Stopping Docker Compose](#stopping-docker-compose)

### Introduction
This code challenge has the objective creating an API to manage equipments and it's points, it allows you to read, create, update and delete equipments and points.

For Front-End the technology used was Angular.

For Back-End the technology used was NodeJs.

For Database the technology used was MongoDB.

### Update Submodules
After cloning this repo, use the command bellow to update the git submodules:

```bash
$ git submodules update --remote
```
    
### Docker Compose

This `docker-compose.yaml` is configured to run MongoDB, NestJs Application and Angular Application(in this order).
Once it's up, you are able to access Front-End and Back-End Application at:

```bash
# Front-End
http://localhost:80/
http://127.0.0.1:80/

# Back-End
http://localhost:3003/
http://127.0.0.1:3003/
```

#### Running Docker Compose

First you need to set your `.env` file in project root:

```bash
# this example works for docker mongo
DB_URI=mongodb://mongodb:27017/db_siemens_test

# this example works for mongo service
DB_URI=mongodb+srv://<user>:<password>@<mongo_service>/<table>
```

Then in the root run:

```bash
$ docker-compose up
```

In case of changes the code, rebuild the docker with:

```bash
$ docker-compose up --build
```


#### Stopping Docker Compose

After stopping all dockers you need to shutdown them with:

```bash
$ docker-compose down
```
