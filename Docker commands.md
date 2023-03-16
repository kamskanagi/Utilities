# UseFul Docker Commands
Docker technology makes it possible to build, distribute, and run applications using containers. 
A Container is a piece of software that packages the code and all of its dependencies so that the application can execute regardless of the environment. 
The container encapsulates the program and its dependencies into a self-contained package that can operate anywhere. 
The absence of physical hardware allows for more efficient use of computing resources. Containers provide virtualization at the operating system level. 
Furthermore, developers may communicate more quickly without having to worry about which software dependencies they need to install.
A container is a runnable image instance. An image is a read-only template containing Docker container creation instructions.
The Docker API or CLI can be used to create, start, stop, move, or destroy containers. A single container can be connected to one or more networks, 
and storage can be attached to it. A new picture can also be produced based on the container’s current state. 
Containers can be shared, guaranteeing that everyone who communicates with it receives the same container and operates in the same manner. 



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
