# Working with Images

## List available Docker images:

```bash
docker image ls
```

## Push an Image to Docker Hub

### Step-1 Login to Docker Hub

```bash
docker login -u <username>
```

### Step-2 Push to Docker Hub

```bash
docker push <username>/<imagename>:<tag>
```

## Pull an Image

```bash
docker pull <username>/<imagename>:<tag>
```

# Working with Containers

## Create and Run a container in interactive mode with a terminal.

```bash
docker run -it <image> bash
```

## Create and run a container in detached mode (background)

```bash
docker run -d <image>
```

## List running containers

```bash
docker container ls
```

_or_

```bash
docker ps
```

## List all containers (both running and stopped containers)

```bash
docker container ls -a

```

_or_

```bash
docker ps -a
```

## Stop a running container

```bash
docker stop <container_id_or_name>
```

## Start a stopped container

```bash
docker start <container_id_or_name>
```

## Restart a container

```bash
docker restart <container_id_or_name>
```

## Remove a container

```bash
docker container rm <container_id_or_name>
```

## View logs of a container

```bash
docker logs <container_id_or_name>
```

## View the last 100 lines of logs

```bash
docker logs --tail 100 <container_id_or_name>
```

## Access a running container’s shell

```bash
docker exec -it <container_id_or_name> bash
```
