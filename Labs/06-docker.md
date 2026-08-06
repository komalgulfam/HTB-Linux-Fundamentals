# 06 - Docker

## Objective

Learn the basics of Docker by installing Docker, building an image, creating containers, and managing them.

---

## Install Docker

```bash
sudo apt install docker.io -y
```

Check Docker status:

```bash
sudo systemctl status docker
```

---

## Create Docker Project

```bash
mkdir my_docker_lab
cd my_docker_lab
nano Dockerfile
```

---

## Dockerfile

```Dockerfile
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y apache2 openssh-server && \
    rm -rf /var/lib/apt/lists/*

EXPOSE 22 80

CMD service ssh start && apache2ctl -D FOREGROUND
```

---

## Build Docker Image

```bash
sudo docker build -t myimage .
```

List available images:

```bash
sudo docker images
```

---

## Run a Container

```bash
sudo docker run -d -p 8080:80 -p 2222:22 --name mycontainer myimage
```

---

## Enter a Running Container

```bash
sudo docker exec -it mycontainer /bin/bash
```

Or create and enter a new interactive container:

```bash
sudo docker run -it myimage /bin/bash
```

Exit the container:

```bash
exit
```

---

## Stop and Start Containers

Stop a container:

```bash
sudo docker stop mycontainer
```

Start it again:

```bash
sudo docker start mycontainer
```

---

## Useful Docker Commands

List images:

```bash
sudo docker images
```

List running containers:

```bash
sudo docker ps
```

List all containers:

```bash
sudo docker ps -a
```

---

## What I Learned

- Installed Docker on Linux.
- Created a Docker project.
- Wrote a basic Dockerfile.
- Built a Docker image.
- Ran containers with port mapping.
- Entered containers using an interactive shell.
- Started and stopped Docker containers.
- Managed Docker images and containers.
```
