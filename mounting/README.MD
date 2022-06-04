# Docker mounting (local directory in container)

## Short description about this action

Mounting a directory into a container is the process of granting access to a container to read the contents of a folder from the main operating system. That is, in fact, providing the container with your information (submitting your scripts for further reproduction in the container).

## step by step

In order to use mounting - in a simple version, it will be enough to run the following command:

```bash
  $ docker run -it -v <MAIN_SYSTEM_DICRECTORY>:<CONTAINER_DIRECOTYR> ...,
```

P.S: I would like to draw attention to the fact that if you run the command from under the CLI, then specifying the current directory via "." will not work correctly. In view of this, the entire path should be indicated in full. (In the future we will consider how to get rid of this).
