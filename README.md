# usersdemo-node-mongo-docker

Basic boilerplate: Docker (docker-compose) contains Node server connected to MongoDB.
The system consists on two services that run in separate containers:

+ NodeJs service based on official node docker image.
+ MongoDB service based on official mongo docker image.


## Demo
Simple User management RESTful API:
`GET /api/users` Get all the users.
`POST /api/users/new`	Create a user.
`GET /api/users/:user_id`	Get a single user.
`PUT /api/users/:user_id`	Update a user with new info.
`DELETE /api/users/:user_id` Delete a user.

```groovy
$ git clone https://github.com/andrewmt/usersdemo-node-mongo-docker.git
$ cd usersdemo-node-mongo-docker
$ docker-compose up
// connect in your browser to <host IP>:3000/api/<...>
```

## Docker
- For MacOs: add the project directory to Docker -> Preferences -> File Sharing
- `docker images`
- `docker ps -a`
- stop all containers: `docker kill $(docker ps -q)`
- remove all containers. `docker rm $(docker ps -a -q)`
- remove all docker images. `docker rmi $(docker images -q)`
- remove all `docker kill $(docker ps -q) & docker rm $(docker ps -a -q) & docker rmi $(docker images -q)`
