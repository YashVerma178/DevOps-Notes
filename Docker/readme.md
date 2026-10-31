# 🐳 Docker — Documentation & Learning Notes

This repository contains my notes and learnings while studying Docker through its official documentation, reference guides, and hands-on practice.

The goal is to understand Docker's core concepts, command-line tools, APIs, file formats, and their practical applications in software development and deployment.

## 📚 Table of Contents

- [Docker Fundamentals](#-docker-fundamentals)
- [File Formats](#-file-formats)
- [Command-Line Interfaces](#-command-line-interfaces-clis)
- [Application Programming Interfaces](#-application-programming-interfaces-apis)
- [Images and Containers](#-images-and-containers)
- [Networking and Storage](#-networking-and-storage)
- [Docker Compose](#-docker-compose)
- [Java and Spring Boot Integration](#-java-and-spring-boot-integration)
- [Learning Resources](#-learning-resources)
- [Learning Progress](#-learning-progress)

## 🐳 Docker Fundamentals

Topics to understand before exploring the detailed reference documentation:

- What is Docker?
- Why is Docker used?
- Containers vs Virtual Machines
- Docker Architecture
- Docker Engine and Docker Desktop
- Docker Images and Containers
- Container Lifecycle

**Official Reference:** [Docker Documentation](https://docs.docker.com/)

## 📄 File Formats

Docker uses configuration files to define how containers are built and how multi-container applications are configured.

### 1. Dockerfile

A Dockerfile contains instructions for building a Docker image, including the environment and commands used to configure the resulting container.

**Topics to explore:**
- Dockerfile syntax
- `FROM`, `RUN`, `WORKDIR`, and `COPY`
- `EXPOSE`, `CMD`, and `ENTRYPOINT`
- Building images
- Dockerfile best practices

📖 **Official Documentation:** [Dockerfile Reference](https://docs.docker.com/reference/dockerfile/)

### 2. Compose File

A Compose file defines the services, networks, volumes, and other configuration needed to run a multi-container application.

**Topics to explore:**
- `compose.yaml` structure
- Services and images
- Port mapping
- Environment variables
- Networks and volumes
- Starting and stopping application services

📖 **Official Documentation:** [Compose File Reference](https://docs.docker.com/reference/compose-file/)

## 💻 Command-Line Interfaces (CLIs)

Docker provides command-line tools for interacting with containers, managing applications, and controlling the Docker daemon.

### 1. Docker CLI

The Docker CLI provides commands for working with Docker images, containers, networks, volumes, and other resources.

**Important commands to learn:**

| Command | Purpose |
|---|---|
| `docker --version` | Display the Docker CLI version |
| `docker pull` | Download an image |
| `docker images` | List local images |
| `docker run` | Create and start a container |
| `docker ps` | List running containers |
| `docker ps -a` | List all containers |
| `docker build` | Build an image |
| `docker stop` | Stop a running container |
| `docker start` | Start an existing container |
| `docker logs` | View container logs |
| `docker rm` | Remove a container |
| `docker rmi` | Remove an image |

📖 **Official Documentation:** [Docker CLI Reference](https://docs.docker.com/reference/cli/docker/)

### 2. Compose CLI

The Compose CLI manages applications consisting of multiple services.

**Important commands to learn:**

| Command | Purpose |
|---|---|
| `docker compose up` | Create and start application services |
| `docker compose down` | Stop and remove application containers and networks |
| `docker compose ps` | List application services and their status |
| `docker compose logs` | View service logs |
| `docker compose build` | Build or rebuild service images |
| `docker compose exec` | Execute a command inside a running service container |

📖 **Official Documentation:** [Compose CLI Reference](https://docs.docker.com/reference/cli/docker/compose/)

### 3. Docker Daemon CLI (`dockerd`)

The Docker daemon is a persistent background process responsible for managing Docker resources and performing container-related operations.

The `dockerd` command starts the Docker daemon.

**Topics to explore:**
- Docker daemon architecture
- Daemon configuration
- Daemon networking
- Logging and troubleshooting
- Communication between the Docker CLI and daemon

📖 **Official Documentation:** [Docker Daemon Reference](https://docs.docker.com/reference/cli/dockerd/)

## 🔌 Application Programming Interfaces (APIs)

Docker provides APIs that allow applications and tools to interact programmatically with Docker services.

### 1. Sandboxes API

The Sandboxes API provides functionality for creating cloud sandboxes, running processes, and managing sandbox resources.

**Topics to explore:**
- Sandbox creation
- Process execution
- Sandbox resource management

📖 **Official Documentation:** [Sandboxes API](https://docs.docker.com/reference/api/sandboxes/latest/)

### 2. Docker Engine API

The Docker Engine API provides programmatic access to the Docker daemon.

It allows compatible applications and tools to interact with Docker Engine resources.

**Topics to explore:**
- API endpoints
- Container management
- Image operations
- Network and volume management
- API requests and responses

📖 **Official Documentation:** [Docker Engine API](https://docs.docker.com/reference/api/engine/)

### 3. Docker Hub API

The Docker Hub API allows applications and tools to interact with Docker Hub.

**Topics to explore:**
- Docker Hub resources
- Repository management
- Authentication
- API requests and responses

📖 **Official Documentation:** [Docker Hub API](https://docs.docker.com/reference/api/hub/latest/)

### 4. Docker Verified Publishers (DVP) Data API

The DVP Data API provides access to analytics data for Docker Verified Publishers.

This API is primarily relevant to publishers and tools that work with publisher analytics.

📖 **Official Documentation:** [DVP Data API](https://docs.docker.com/reference/api/dvp/latest/)

### 5. Registry API

The Registry API supports interactions with Docker Registry services.

**Topics to explore:**
- Image repositories
- Image manifests
- Registry endpoints
- Pushing and pulling images
- Registry authentication

📖 **Official Documentation:** [Docker Registry API](https://docs.docker.com/reference/api/registry/latest/)

## 🖼️ Images and Containers

Docker images are templates used to create containers. Containers are running or stopped instances created from images.

**Topics to explore:**
- Image layers and caching
- Pulling images from registries
- Building custom images
- Container lifecycle
- Environment variables
- Container logs
- Resource management

📖 **Learning Resource:** [Docker Get Started](https://docs.docker.com/get-started/)

## 🌐 Networking and Storage

### Networking
- Bridge networks
- Custom networks
- Container-to-container communication
- Port mapping
- Network inspection

### Storage
- Docker volumes
- Bind mounts
- Persistent application data
- Volume management
- Sharing data between containers

📖 **Official Documentation:** [Docker Networking](https://docs.docker.com/engine/network/)

📖 **Official Documentation:** [Docker Storage](https://docs.docker.com/engine/storage/)

## ⚙️ Docker Compose

Docker Compose simplifies the configuration and management of multi-container applications.

**Topics to explore:**
- Defining services
- Configuring application networks
- Managing volumes
- Using environment variables
- Building and running multiple services
- Troubleshooting application containers

📖 **Official Documentation:** [Docker Compose](https://docs.docker.com/compose/)

## ☕ Java and Spring Boot Integration

As part of my backend development learning, I will explore how Docker can be used with Java and Spring Boot applications.

**Planned topics:**
- Creating a Dockerfile for a Spring Boot application
- Building a Docker image for a Java application
- Running Spring Boot applications in containers
- Connecting an application to a database
- Using Docker Compose for multi-container applications
- Multi-stage Docker builds
- Preparing containerized applications for cloud deployment

📖 **Official Documentation:** [Spring Boot with Docker](https://spring.io/guides/gs/spring-boot-docker)

## 📖 Learning Resources

- [Docker Documentation](https://docs.docker.com/)
- [Docker Reference](https://docs.docker.com/reference/)
- [Dockerfile Reference](https://docs.docker.com/reference/dockerfile/)
- [Compose File Reference](https://docs.docker.com/reference/compose-file/)
- [Docker CLI Reference](https://docs.docker.com/reference/cli/docker/)
- [Docker Engine API](https://docs.docker.com/reference/api/engine/)
- [Docker Get Started Guide](https://docs.docker.com/get-started/)
- [Docker Workshop](https://docs.docker.com/get-started/workshop/)

## ✅ Learning Progress

- [ ] Docker Fundamentals
- [ ] Docker Images and Containers
- [ ] Dockerfile Reference
- [ ] Compose File Reference
- [ ] Docker CLI
- [ ] Compose CLI
- [ ] Docker Daemon
- [ ] Docker Networking
- [ ] Docker Volumes
- [ ] Docker Compose
- [ ] Docker APIs
- [ ] Java and Spring Boot Containerization
- [ ] Multi-Stage Builds
- [ ] Containerized Application Deployment

## 👨‍💻 About This Repository

This repository documents my progress in learning Docker through official documentation and practical implementation.

The notes will be updated as I explore new concepts, experiment with commands, build applications, and solve technical problems.

**Learning approach:** Read → Understand → Practise → Document → Revise.

---

*These notes are for educational purposes. The official Docker documentation remains the primary reference for detailed specifications, supported commands, and API behavior.*