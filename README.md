# Common Docker Commands

- Start docker

```bash
    systemctl start docker  # Linux
    open -a Docker  # macOS
```

- Check Docker Version

```bash
    docker --version
```

# Working with Containers

- List Running Containers:

```bash
    docker ps
```

- List All Containers (Running + Stopped):

```bash
    docker ps -a
```

- Run a Container (starts and attaches):

```bash
    docker run <image_name>
```

- Run in Detached Mode:

```bash
    docker run -d <image_name>
```

- Run with Port Mapping:

```bash
    docker run -p <host_port>:<container_port> <image_name>
```

- Stop a Running Container:

```bash
    docker stop <container_id>
```

- Start a Stopped Container:

```bash
    docker start <container_id>
```

- Remove a Stopped Container:

```bash
    docker rm <container_id>
```

# Images

- List Docker Images:

```bash
    docker images
```

- Pull an Image from Docker Hub:

```bash
    docker pull <image_name>
```

- Build an Image from Dockerfile:

```bash
    docker build -t <image_name> .
```

- Tag an Image:

```bash
    docker tag <image_id> <new_image_name>:<tag>
```

- Remove an Image:

```bash
    docker rmi <image_id>
```

# Container Management

- View Logs of a Container:

```bash
    docker logs <container_id>
```

- Access a Running Container (Interactive Shell):

```bash
    docker exec -it <container_id> /bin/bash
```

- Copy Files from Container to Host:

```bash
    docker cp <container_id>:<path_inside_container> <host_path>
```

# Docker Networks

- List Networks:

```bash
    docker network ls
```

- Create a Network:

```bash
    docker network create <network_name>
```

- Connect a Running Container to a Network:

```bash
    docker network connect <network_name> <container_id>
```

# Docker Compose

- Start Services in Detached Mode:

```bash
    docker-compose up -d
```

- Stop Services:

```bash
    docker-compose down
```

- Build and Start Containers:

```bash
    docker-compose up --build
```

# Inspecting and Monitoring

- Inspect Container Details:

```bash
    docker inspect <container_id>
```

- Display Resource Usage (CPU, Memory):

```bash
    docker stats
```

# Volumes

- List Volumes:

```bash
    docker volume ls
```

- Create a Volume:

```bash
    docker volume create <volume_name>
```

- Mount a Volume (during docker run):

```bash
    docker run -v <volume_name>:<path_inside_container> <image_name>
```

## 💡 Use `docker system prune` to remove unused containers, networks, and images.

Source: [keshav Sandhu Docker Cheat-sheet for beginners](https://dev.to/keshav___dev/docker-cheat-sheet-for-beginners-18mo?ref=dailydev)
