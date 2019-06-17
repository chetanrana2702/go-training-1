# Docker

*Containers are standalone software packages that bundle an application with all its dependencies, tools, libraries, runtime, configuration files, and anything else necessary to run the application.*

*Containers abstract away the application from any of the environments that they will run on. That means, containerized apps run consistently across environments from dev to staging to production.*

https://www.docker.com/get-started

Golang official docker images
- https://hub.docker.com/_/golang

 
## Docker containers with Go and RabbitMq
#### Example:
- See: [docker-compose.yml](../src/16-docker/docker-compose.yml) and the [example configuration](../src/16-docker/)
- Go to path `src/16-docker` and execute:
    - `docker-compose up`
- Visit:
    - [http://localhost:8080](http://localhost:8080) to send a message
    - [http://localhost:15672](http://localhost:15672) is the RabbitMq admin (admin/1234)

#### Commands found in the Dockerfile

```
# copy the local project code into a directory in work dir directory
COPY web-app.go .

# set this to the working directory so all subsequent commands will run from this directory
WORKDIR /go/src/app

# install all dependencies
RUN go get ./

# build the binary
RUN go build
```

## Related links
- [Building Docker Containers for Go Applications](https://www.callicoder.com/docker-golang-image-container-example/)
- [Dockerizando tu aplicación en go, Friends Of Go (spanish)](https://blog.friendsofgo.tech/posts/dockerizando-tu-aplicacion-en-go/)
- [Building Docker Containers for Go Applications](https://www.callicoder.com/docker-golang-image-container-example/#creating-a-simple-golang-app)
- [Docker dev environment with Go Modules and live code reloading](https://threedots.tech/post/go-docker-dev-environment-with-go-modules-and-live-code-reloading/)
- [Golang and Docker for development and production](https://medium.com/statuscode/golang-docker-for-development-and-production-ce3ad4e69673)
- [Docker RUN vs CMD vs ENTRYPOINT](https://goinbigdata.com/docker-run-vs-cmd-vs-entrypoint/)

Todd McLeod documentation and some examples:
- https://github.com/GoesToEleven/golang-web-dev/tree/master/043_docker

#### RabbitMq
- [Send Messages to RabbitMq with Go](18-rabbitmq.md)

