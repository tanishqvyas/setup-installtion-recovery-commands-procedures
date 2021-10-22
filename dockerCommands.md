# Docker Commands Cheatsheet

This file contains some useful commands, terminologies and setup instructions related to docker.

**NOTE** : All commands and setup instructions will be executed on `Ubuntu 20.04` aka `Focal Fossa`.


## Installing Docker on Ubuntu 20.04


## Commands Cheatsheet

Following commands can come in hands when working with Docker.

### Checking the version of Docker

```bash
sudo docker version
```

or 

```bash
sudo docker --version
```

### Running Hello-World for Docker

```bash
sudo docker run hello-world
```

**New Syntax**

This added keyword `container` is context keyword

```bash
sudo docker container run hello-world
```

Some images do come with default commands and some do not. 

Thus we can specify our own custom startup commands

Example:

```bash
sudo docker container run busybox ls
```

```bash
sudo docker container run busybox echo "Hi my name is Tanishq"
```

### List all the Containers ever created

```bash
sudo docker container ls -a
```

### List all Running Containers

```bash
sudo docker container ls
```

### Delete a Container

```bash

```

### Create and Start a Container

**1. This command creates the container from the image. Once it runs, it returns the ID of the container just created**

```bash
sudo docker container create hello-world
```

**2. This command starts a container that is created / exists. The `-a` basically means that this should print any output from the container right into our terminal.**


```bash
sudo docker container start -a <Container-ID>
```

**3. The `run` command is basically a combination of the above two commands**

```bash
sudo docker container run hello-world
```

### Remove all the Containers

The following command removes everything including cache.

```bash
sudo docker system prune --all
```

### View Logs

```bash
sudo docker container logs <Container-ID> 
```

### Stopping a Container

```bash
sudo docker container stop <Container-ID>
```

Docker containers which ignore the stop command, are provided a max of `10 seconds` to perform any kind of cleanup it needs to. Post that Docker just kills the container.


### Killing a Container

```bash
sudo docker container kill <Container-ID>
```

### Removing a Container

```bash
sudo docker container rm <Container-ID>
```

Sometimes this will fail if there are processes running inside a container. Thus if we wish to remove forcefully

```bash
sudo docker container rm -f <Container-ID>
```

### Inspect a Container

```bash
sudo docker container inspect <Container-ID>
```

### Run a command in an Already Running Container

The `-it` flag is to ensure we can interact and provide inputs

```bash
sudo docker container exec -it <Container-ID> <Programme Name>
```

To get access to the container

```bash
sudo docker container exec -it <Container-ID> sh
```

### Start a container with Shell

```bash
sudo docker container run -it <Image Name> sh
```


## Creating Custom Images in Docker


### Viewing Images

```bash
sudo docker image ls
```

### Removing Images

```bash
sudo docker image rm <Image-ID>
```

### Creating Image using Dockerfile

**Step 1 : Create a file by the name `Dockerfile`**

The name of the file must be `Dockerfile`. Any changes in the name will result in failure of further procedures.

**Example:**

```Dockerfile
FROM alpine:latest
RUN apk add --update redis
CMD ["redis-server"]

# This is a Comment
```

**Step 2 : Building image from Dockerfile**

The `-t` flag allows us to tag our image with a friendly name for repository

```bash
sudo docker build -t <Custom-Name> <Path-To-Dockerfile-Dir>
```


