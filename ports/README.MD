# Docker container ports

## Short description about container ports

P.S The information is provided from the website [badcode](https://badcode.ru).

Docker allows us to access some of the container ports by throwing it outside (into the main operating system). By default, we cannot reach any of the container ports. However, in Dockerfile, the `EXPOSE` option allows us to declare which of the ports we can access from the main operation system.

To do this, in a quick way, let's run the Docker image of php-apache, which runs on port 80.

To begin with, create a new apache folder (go to it apache cd), in which we will create a file index.php on the basis of which we will understand that everything works.

## Simple configuration for ports

```Dockerfile
FROM php:7.4-apache
WORKDIR /var/www/html
COPY . /var/www/html
EXPOSE 80
```