# sensu-backend build

Docker container to build sensu-backend from source and uploads it on an artifact server ([docker-hub](https://hub.docker.com/repository/docker/elfranne/sensu-backend-build)):

```sh
docker run  -e BACKEND_VERSION='v6.12.0' -e ARTIFACT_URL='https://repo.example.org' -e ARTIFACT_USER_PASSWORD='user:password' elfranne/sensu-backend-build:jammy
```

To update/create the docker image

```sh
docker login --username elfranne
docker build - < jammy -t elfranne/sensu-backend-build:jammy
docker push elfranne/sensu-backend-build:jammy
```

This is basically a copy of the Debian Golang container from the lovely people at [docker-library](https://github.com/docker-library/golang/) with a few changes.

Same license as [docker-library](https://github.com/docker-library/golang/)
