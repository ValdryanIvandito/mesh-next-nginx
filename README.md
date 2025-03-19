# Docker Installation on Ubuntu

## Step-1 Update Ubuntu System

```bash
sudo apt update && sudo apt upgrade -y
```

## Step-2 Install Dependencies

```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

## Step-3 Add Docker’s official GPG key

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```

## Step-4 Add Docker’s official APT repository

```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```

## Step-5 Install Docker

```bash
sudo apt install -y docker-ce docker-ce-cli containerd.io
```

## Step-6 Verify Docker Installation & Check Docker Version

```bash
docker --version
```

## Step-7 Start & ensure Docker starts automatically on boot

```bash
sudo systemctl enable docker
```

## Step-8 Check Docker Status

```bash
sudo systemctl status docker
```

## Step-9 Manage Docker as a non-root user

```bash
sudo usermod -aG docker $USER
```

## Step-10 Reboot Server

```bash
sudo reboot
```

## Start Docker (Optional)

```bash
sudo systemctl start docker
```

## Restart Docker (Optional)

```bash
sudo systemctl restart docker
```

## Stop Docker (Optional)

```bash
sudo systemctl stop docker
```

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

# References

1. [Datacamp: Install Docker on Ubuntu](https://www.datacamp.com/tutorial/install-docker-on-ubuntu)

command: whereis docker
output: /snap/bin/docker

command: crontab -e
chose nano editor

# Dijalankan dua bulan sekali di awal bulan jam 5 pagi

0 5 1 _/2 _ sudo /snap/bin/docker compose -f ./docker-compose.yaml up certbot

# Dijalankan setiap hari pukul jam 12 malam

0 0 \* \* \* sudo /snap/bin/docker compose -f ./docker-compose.yaml up certbot

Cek cron job
systemctl status cron
