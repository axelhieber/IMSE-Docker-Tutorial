# Docker Demo

I created this small Docker demo project as part of my tutor job for the course _Information Management & Systems Engineering_ at Uni Vienna. The goal is to show the basics of setting up and using Docker.

# Basic Docker Commands
## Overview

| Command | Description |
|---|---|
| `docker ps` | List running containers. |
| `docker ps -a` | List all containers, including stopped ones. |
| `docker rm <container>` | Remove a stopped container. |
| `docker images` | List locally available Docker images. |
| `docker image rm <image>` | Remove a Docker image. |
| `docker image pull <image>` | Download or Update a Docker image from an image registry like Docker hub |
| `docker run <image>` | Create and start a new container. |
| `docker run -d -p 8080:80 <image>` | Map host port 8080 to container port 80. |
| `docker start <container>` | Start an existing stopped container. |
| `docker start -ai <container>` | Start an existing container and attach to its input and output. |
| `docker stop <container>` | Stop a running container. |
| `docker exec -it <container> /bin/bash` | Open an interactive shell inside a running container. - similar to ssh |


> **Note:**
> - **Image:** An image reference can include a registry, a publisher/namespace, a repository name, and a tag.
>   - `python:3` – Python repository, tag `3`.
>   - `python:3.14` – Python repository, tag `3.14`.
>   - `username/myapp:1.0` – Publisher `username`, repository `myapp`, tag `1.0`.
>   - If no tag is specified, `latest` is used by default.
> - **Container:** `<container>` can refer to either a container name or a container ID (including a unique shortened ID).

## `docker run` Options

| Option | Description |
|---|---|
| `-i` | Keep standard input open. |
| `-t` | Allocate a pseudo-terminal. |
| `-d` | Run in detached mode (background). |
| `-p <host>:<container>` | Publish a container port on the host. |
| `--name <name>` | Assign a name to the container. |
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



# Soruce

https://github.com/StJonas/Docker-Tutorial
