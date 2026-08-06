# Docker vs LXC

## What is Containerization?

Containerization is a virtualization technology that allows applications or operating systems to run in isolated environments while sharing the host system's kernel.

Containers are lightweight, start quickly, and consume fewer resources than traditional virtual machines.

---

## What is Docker?

Docker is an application container platform.

It packages an application together with its dependencies into an image, which can then be run consistently on any system with Docker installed.

Docker is mainly used for:

- Application deployment
- Microservices
- DevOps
- Cloud environments
- Software testing

---

## What is LXC?

LXC (Linux Containers) provides a lightweight operating-system-level virtualization environment.

Unlike Docker, an LXC container behaves much more like a complete Linux system.

It can run:

- systemd
- Multiple services
- Background daemons
- Multiple users

---

## Docker Architecture

Docker consists of:

- Docker Engine
- Docker Images
- Docker Containers
- Docker Registry (Docker Hub)

Workflow:

Dockerfile
↓

Docker Image
↓

Docker Container

---

## LXC Architecture

Host Linux Kernel
↓

LXC Container

↓

Complete Linux User Space

Each LXC container behaves like a small Linux machine.

---

## Docker vs LXC

| Docker | LXC |
|---------|-----|
| Application container | System container |
| Runs a single application | Runs a complete Linux system |
| Lightweight | Lightweight |
| Uses Docker Engine | Uses LXC tools |
| Popular in DevOps | Popular for system virtualization |

---

## Advantages of Docker

- Fast startup
- Portable
- Lightweight
- Easy deployment
- Large ecosystem
- Docker Hub support

---

## Advantages of LXC

- Full Linux environment
- Multiple services inside one container
- Better for learning Linux administration
- Low resource usage
- Easy system isolation

---

## Common Use Cases

### Docker

- Web applications
- APIs
- Databases
- CI/CD pipelines
- Cloud deployments

### LXC

- Linux labs
- Testing operating systems
- Security practice
- Lightweight virtual servers

---

## Similarities

- Both use the host Linux kernel.
- Both are lightweight.
- Both provide isolation.
- Both consume fewer resources than virtual machines.

---

## Differences

- Docker focuses on applications.
- LXC focuses on complete Linux systems.
- Docker usually runs one main process.
- LXC can run multiple services simultaneously.

---

## Exam Notes

Remember:

- Docker = Application Container
- LXC = System Container
- Both share the host kernel.
- Containers are lighter than virtual machines.
- Docker is common in DevOps and cloud environments.
- LXC is useful for Linux administration and security labs.
