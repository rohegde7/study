# Docker from boot.dev

### Topics
- "Docker server" or "Docker Daemon" -> This listens to requests from the desktop app and executes them. If this isn't running nothing else will work. Commands from terminal goto this (hosted by docker desktop app)
- `Docker Hub` is the official cloud service for storing and sharing Docker images
- `container`
- `Storage Volumes`

### Commands
- `docker pull <image-name>`
  -   ex: docker pull docker/getting-started
- `docker images`
- `docker run`
- `docker run -d -p hostport:containerport namespace/name:tag`
  - ex: docker run  docker/getting-started
  - docker run -d -p 8080:1234 docker/getting-started:latest
  - `-d`: Run in detached mode (doesn't block your terminal)
  - `-p`: Publish a container's port to the host (forwarding). 8080 is our local machine's port. 1234 is the container's port. so `localhost:8080` will goto port `1234` on which the container is listening/running.
  - `-e`: Used to set environment variables -> `-e NODE_ENV=development -e url=http://localhost:3001`
  - `-v`: Mounts the volume to a folder inside the container -> `-v ghost-vol:/var/lib/ghost ghost` -> `-v <volume-name>:<path-inside-container>`.`ghost-vol` is the volume name. `/var/lib/ghost` is the path in which the image/container actually writes data when it's running. `ghost` is the name of the image.
  - `hostport`: The port on your local machine
  - `containerport`: The port inside the container
  - `namespace/name`: The name of the image (usually in the format username/repo)
  - `tag`: The version of the image (often latest)
- `docker ps` -> to see the running containers. `-a` -> all. Option shows the stopped containers as well.
- `docker stop CONTAINER_ID`
- `docker start CONTAINER_ID` -> start the already existing container
- `docker restart <CONTAINER_ID>`
- `docker kill CONTAINER_ID`
- `docker volume create ghost-vol` -> Creates a volume outside all docker containers
- `docker volume ls`
- `docker volume inspect <VOLUME_NAME>`


### Interview Questions
- Why Are Containers Lightweight? as compared to VMs


### Imp things

#### Containers and Volumes
- A container's file system is read-write, but when you delete a container, and start a new one from the same image, that new container starts from scratch again with a copy of the image. All stateful changes are lost.
- A volume's file system is read-write, but it lives outside a single container. If a container uses a volume, then stateful changes can be persisted to the volume even if the container is deleted.
- Volumes are often used by applications like Ghost, Grafana, or WordPress to persist data so that when a container is deleted and a new one is created the state of the application isn't lost. Containerized applications are typically thought of as ephemeral (temporary). If your application breaks just because you deleted and recreated a container... it's not a very good containerization!
- 


### To recap / learn 
- `Completion`




### Future topic yet not learnt
- `image layers`
- Isolate containers with a user `namespace`


### Doubts
- 
- 
