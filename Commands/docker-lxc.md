# Docker & LXC

This file contains the Docker and Linux Container (LXC) commands practiced during the Hack The Box Academy Linux Fundamentals module.

---

# Docker Installation

| Command | Description |
|---------|-------------|
| `sudo apt install docker.io -y` | Install Docker |
| `sudo systemctl status docker` | Check Docker service status |

---

# Building Docker Images

| Command | Description |
|---------|-------------|
| `mkdir my_docker_lab` | Create project directory |
| `cd my_docker_lab` | Enter project directory |
| `nano Dockerfile` | Create Dockerfile |
| `sudo docker build -t myimage .` | Build Docker image |
| `sudo docker images` | List Docker images |

---

# Running Containers

| Command | Description |
|---------|-------------|
| `sudo docker run -d -p HOST_PORT:80 --name mycontainer myimage` | Run container in background |
| `sudo docker run -it myimage /bin/bash` | Start an interactive container |
| `sudo docker exec -it mycontainer /bin/bash` | Open a running container |
| `sudo docker stop mycontainer` | Stop a container |
| `sudo docker start mycontainer` | Start a stopped container |
| `exit` | Exit the container shell |

---

# Dockerfile Example

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

# Linux Containers (LXC)

| Command | Description |
|---------|-------------|
| `sudo apt install lxc lxc-templates -y` | Install LXC |
| `sudo lxc-create -n mycontainer -t download -- -d ubuntu -r 22.04 -a amd64` | Create a new LXC container |
| `sudo lxc-ls -f` | List containers |
| `sudo lxc-start -n mycontainer` | Start container |
| `sudo lxc-attach -n mycontainer` | Enter container |
| `sudo lxc-stop -n mycontainer` | Stop container |

---

# LXC Configuration

Configuration file:

```
/etc/lxc/default.conf
```

Example:

```
lxc.cgroup2.cpu.weight = 512
lxc.cgroup2.memory.max = 512M
```

Reload configuration:

```bash
sudo systemctl restart lxc
sudo systemctl daemon-reload
```

---

## Skills Practiced

- Docker installation
- Building Docker images
- Running containers
- Dockerfile basics
- LXC container management
- Resource allocation
