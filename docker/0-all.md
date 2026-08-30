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
  - docker run -d -p 8965:80 docker/getting-started:latest
  - `-d`: Run in detached mode (doesn't block your terminal)
  - `-e`: Used to set environment variables -> `-e NODE_ENV=development -e url=http://localhost:3001`
  - `-p`: Publish a container's port to the host (forwarding)
  - `-v`: Mounts the volume to a folder inside the container -> `-v ghost-vol:/var/lib/ghost ghost`
  - `hostport`: The port on your local machine
  - `containerport`: The port inside the container
  - `namespace/name`: The name of the image (usually in the format username/repo)
  - `tag`: The version of the image (often latest)
- `docker ps` -> to see the running containers
- `docker stop CONTAINER_ID`
- `docker start CONTAINER_ID` -> start the already existing container
- `docker kill CONTAINER_ID`
- `docker volume create ghost-vol`
- `docker volume ls`
- `docker volume inspect ghost-vol`


### Interview Questions
- Why Are Containers Lightweight? as compared to VMs
- 



### To recap / learn 
- `Completion`




### Future topic yet not learnt
- `image layers`
- Isolate containers with a user `namespace`


### Doubts
- why is disk size bigger than content size ? -> try command docker images
- 
