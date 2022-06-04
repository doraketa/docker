# Dockerfile

## Dockerfile short description:

Dockerfile is a kind of recipe in the Docker kitchen. It allows you to recreate the environment that the developer had at the time of development. Basically, we have two ways:

- To recreate the state, which will be simply useless, since we will simply return to the state of the developer's machine at the time of delivery;
- Recreate completely the environment in which the development took place (step by step);

## Main dockerfile commands:

| command   | Description                                                      |
| :-------- | :-------------------------                                       |
| `FROM`  | This is a command for images switching (f.e - php:7.4-cli / ubuntu:20.04 etc.).                 |
| `COPY`  | This is a command for copying file from our system into container system.                 |
| `RUN`  | This is a command for executing shell-command from container terminal.                 |
| `CMD`  | This is a command to execute the specified list of commands every time the container is started again.                 |
| `ENTRYPOINT`  | This command provides commands and arguments for the running container.                 |
| `WORKDIR`  | This command creates a folder if it is not created, and moves to it. Similar to executing `mkdir /var/www/html && cd /var/www/html commands`.                 |
| `EXPOSE`  | Allowing port access to the main operating system.                 |