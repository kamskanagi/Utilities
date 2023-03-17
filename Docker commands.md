# UseFul Docker Commands
Docker technology enables the building, distribution, and execution of applications using containers, which package the application code and dependencies for portability and efficient use of computing resources. Containers provide operating system-level virtualization and can be created, started, stopped, moved, or destroyed using the Docker API or CLI. Containers can be connected to networks and storage, and their current state can be used to create new images. Containers can be shared, ensuring consistent behavior across multiple environments. Below are some of the most useful docker commands.



### Working with images:
- `docker build`: Build an image from a Dockerfile
- `docker images`: List all locally available images
- `docker rmi`: Remove an image
- `docker pull`: Pull an image from a registry
- `docker push`: Push an image to a registry

### Working with containers:
- `docker run`: Create a new container from an image and start it
- `docker ps`: List all running containers
- `docker stop`: Stop a running container
- `docker start`: Start a stopped container
- `docker rm`: Remove a stopped container
- `docker logs`: View the logs of a container
- `docker exec`: Run a command in a running container
- `docker attach`: Attach to a running container

### Working with networks:
- `docker network create`: Create a new network
- `docker network ls`: List all networks
- `docker network inspect`: Inspect a network
- `docker network connect`: Connect a container to a network
- `docker network disconnect`: Disconnect a container from a network

## Working with volumes:
- `docker volume create`: Create a new volume
- `docker volume ls`: List all volumes
- `docker volume inspect`: Inspect a volume
- `docker volume rm`: Remove a volume
- `docker run -v`: Mount a volume in a container

### Working with Docker Compose:
- `docker-compose up`: Start a set of containers defined in a docker-compose.yml file
- `docker-compose down`: Stop and remove the containers started with docker-compose up
- `docker-compose ps`: List all containers managed by Docker Compose
- `docker-compose logs`: View the logs of containers managed by Docker Compose
