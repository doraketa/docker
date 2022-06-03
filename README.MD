
# Simple docker description (~5 minutes)

Hello! This is my repository for docker. Here and now I will write notes necessary for working with docker, as well as technical nuances for various kinds of projects.

## Docker installation (only linux)

In order to install Docker on debian-like systems, we need to use the following list of commands in turn:

#### Step by step:

To begin with, we need to completely update the entire list of packages and get all the updates to our system/kernel:

```sh
  $ apt-get upgrade && apt-get update
```

And also install additional packages that are necessary to work with remote repositories. To install these packages, run the command:

```sh
  $ apt install ca-certificates curl gnupg lsb-release -y
```

Then, we need to download and add the PGP key of the Docker repository:

```sh
  $ curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

To add a Docker repository, run the command:

P.S: This is the most convenient method for automatically substituting the version of your OS. (taken from the website [losst.ru](https://losst.ru)).


```sh
  $ echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Then, after we have added the Docker repositories, we try to update the system again:

```sh
  $ apt-get update && apt-get upgrade
```

Installing additional packages for Docker:

```sh
  $ sudo apt install docker-ce docker-ce-cli containerd.io -y
```

Initially, our Docker will not know that it needs to be launched together with the system (optional), and after installation it will not be launched. Let's do it:

```sh
  $ systemctl start docker  # This command will launch Docker
  $ systemctl enable docker # This command will add Docker to the startup
```

As the portal suggests [losst.ru](https://losst.ru), mentioned above - initially Docker is executed only from the root user. It is advisable to fix this. This is fixed by adding the user to the "Docker" group:

```sh
  $ groupadd docker
  $ usermod -aG docker $USER
```

Done! Now we can run our "Hello-World" container to check Docker:

```sh
  $ docker run hello-world
```
