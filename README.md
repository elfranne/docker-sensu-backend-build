
Docker container to build sensu-backend from source and uploads it on a artifact server ([docker-hub](https://hub.docker.com/repository/docker/elfranne/sensu-backend-build)): 


```
docker run  -e BACKEND_VERSION='v6.4.0' -e ARTIFACT_URL='https://repo.example.org' -e ARTIFACT_USER_PASSWORD='user:password' elfranne/sensu-backend-build:bionic
```


To update/create the docker
```
docker login --username elfranne
docker build - < bionic -t elfranne/sensu-backend-build:bionic
docker push elfranne/sensu-backend-build:bionic
```

This is basically a copy of the Debian Golang container from the lovely people at [docker-library](https://github.com/docker-library/golang/) with a few changes.

Same license as [docker-library](https://github.com/docker-library/golang/)
