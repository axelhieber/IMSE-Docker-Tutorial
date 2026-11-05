# Docker Demo

I created this small Docker demo project as part of my tutor job for the course _Information Management & Systems Engineering_ at Uni Vienna. The goal is to show the basics of setting up and using Docker.

# Basic Docker Commands
## Overview

| Command | Description |
|---|---|
| `docker ps` | List running containers. |
| `docker ps -a` | List all containers, including stopped ones. |
| `docker images` | List locally available Docker images. |
| `docker image rm <image>` | Remove a Docker image. |
| `docker image pull <image>` | Download or Update a Docker image from an image registry like Docker hub |
| `docker run <image>` | Create and start a new container. |
| `docker run -d -p 8080:80 <image>` | Map host port 8080 to container port 80. |
| `docker start <container>` | Start an existing stopped container. |
| `docker start -ai <container>` | Start an existing container and attach to its input and output. |
| `docker stop <container>` | Stop a running container. |
| `docker exec -it <container> /bin/bash` | Open an interactive shell inside a running container. - similar to ssh |
| `docker rm <container>` | Remove a stopped container. |

> **Note:** Docker `<image>` references follow this format:
> `[registry/][namespace/]repository[:tag]`
>
> Examples:
> - `python` – Official Python image, implicitly using the `latest` tag.
> - `python:latest` – Official Python image.
> - `python:3` – Official Python image, tag `3`.
> - `python:3.14` – Official Python image, tag `3.14`.
> - `ghcr.io/username/myapp:1.0` – Registry `ghcr.io`, namespace `username`, repository `myapp`, tag `1.0`.
>
> Docker defaults to Docker Hub. Official images do not require an explicit namespace.
>
> `<container>` can be either a container name or a container ID.




## Expanded

| Command | Description |
|---|---|
| `docker logs <container>` | Display the logs of a container. |
| `docker inspect <container>` | Display detailed container information, including configuration, networking, and mounted volumes. |
| `docker volume ls` | List all Docker volumes. |
| `docker volume inspect <volume>` | Display detailed information about a volume, including its mountpoint. |
| `docker volume rm <volume>` | Remove an unused Docker volume. |
| `docker network ls` | List all Docker networks. |
| `docker network create <network>` | Create a new Docker network. |
| `docker network rm <network>` | Remove an unused Docker network. |
| `docker volume prune` | Remove all unused anonymous volumes. |
| `docker volume prune -a` | Remove all unused volumes, including named volumes. |


## `docker run` Options

| Option | Description |
|---|---|
| `-i` | Keep standard input open. |
| `-t` | Allocate a pseudo-terminal. |
| `-d` | Run in detached mode (background). |
| `-p <host>:<container>` | Publish a container port on the host. |
| `-v <source>:<target>` | Mount a host directory or Docker volume into the container. |
| `-h <hostname>` | Set the container's hostname. |
| `-e <key>=<value>` | Set an environment variable. |
| `--name <name>` | Assign a name to the container. |
| `--network <network>` | Connect the container to a Docker network. |
| `--rm` | Automatically remove the container when it exits. |

> **Note:** `docker run` uses the locally available image.
> If the image is not available locally, Docker attempts to pull it
> from a registry. Use `docker pull <image>` to explicitly download
> the latest available version for the specified tag.


## `docker start` Options

| Option | Description |
|---|---|
| `-a` | Attach to the container's output (STDOUT/STDERR). |
| `-i` | Attach standard input (STDIN). |


## `docker exec` Options

| Option | Description |
|---|---|
| `-i` | Keep standard input open. |
| `-d` | Run the command in the background (detached mode). |
| `-u <user>` | Execute the command as a specific user. |
| `-w <directory>` | Set the working directory for the command. |
| `-e <key>=<value>` | Set an environment variable. |

# Demo Overview

The Stack will be Postgresql, Python/Flask as the backend an Nginx/HTML&JS as the frontend.

docker exec -it mariadb-test -u root -p

# Soruce

https://github.com/StJonas/Docker-Tutorial
