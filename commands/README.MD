# Docker commands example

## Main commands list:

| command   | Description                                                      |
| :-------- | :-------------------------                                       |
| `$ docker`  | This is a command for interacting with Docker.                 |
| `$ docker pull`  | This is the command to download the image.                 |
| `$ docker images`  | This is the command to output images list in your terminal.                 |
| `$ docker run`  | This is the command to start the container.                 |
| `$ docker ps`  | This is a command to check the list of running containers.                 |
| `$ docker start <container-id>`  | This command starts the container by its ID.                 |
| `$ docker stop <container-id>`  | This command stop the container by its ID.                 |
| `$ docker rm <container-id>`  | This command delete the container by its ID.                 |
| `$ docker build <DOCKERFILE_PATH> --tag <IMAGE_NAME>`  | This command create an docker image from DockerFile.                 |

## Additional commands list:

| command   | Description                                                      |
| :-------- | :-------------------------                                       |
| `$ docker run -it ubuntu:XX.XX /bin/bash`  | This command will launch the interactive mode of using /bin/bash in our running container.                 |
| `$ docker run -p <HOST_PORT>:<CONTAINER_PORT>`  | This command allows you to start the container, while sharing the port to an external operating system.                 |