Docker Commands

## Build Docker Image
```
docker build -t react-docker .
```

## Run Docker Image
```
docker run -p 3000:3000 react-docker
```

## Run Docker Image in Background
```
docker run -d -p 3000:3000 react-docker
```

## List Docker Images
```
docker images
```

## List Running Docker Containers
```
docker ps
```

## Stop Docker Container
```
docker stop <container-id>
```

## Remove Docker Container
```
docker rm <container-id>
```

## Remove Docker Image
```
docker rmi <image-id>
```

## Remove All Docker Images
```
docker rmi $(docker images -q)
```
```

## Remove All Docker Containers
```
docker rm $(docker ps -a -q)
```

## Remove All Stopped Docker Containers
```
docker container prune // or docker rm $(docker ps -a -q)
```

## Remove All Docker Images
```
docker rmi $(docker images -q)
```

## Login to Docker Hub
```
docker login
```
## Delete Volume
```
docker volume rm $(docker volume ls -q)
```

## Delete All Volumes
```
docker volume prune
```

## View Docker Volume
```
docker volume ls
```

## View Docker Logs
```
docker logs <container-id>
```

## View Docker Logs in Realtime
```
docker logs -f <container-id>
```

## auto update docker container
```
docker run -p 5173:5173 -v "$(pwd):/app" -v /app/node_modules react-docker
