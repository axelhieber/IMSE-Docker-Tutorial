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
| `docker start -ai` | |



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


# Demo Overview

The Stack will be Postgresql, Python/Flask as the backend an Nginx/HTML&JS as the frontend.



# Soruce

https://github.com/StJonas/Docker-Tutorial
