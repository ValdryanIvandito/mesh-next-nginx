# Docker Commands

## Working with Images

### List available Docker images:

```bash
docker image ls
```

### Push an Image to Docker Hub

#### Step-1 Login to Docker Hub

```bash
docker login -u <username>
```

#### Step-2 Push to Docker Hub

```bash
docker push <username>/<imagename>:<tag>
```

### Pull an Image

```bash
docker pull <username>/<imagename>:<tag>
```
