# Scheduling Certbot Certificate Renewal

## Step-1 Find docker path location:

```bash
whereis docker
```

Example output:

```bash
/usr/bin/docker
```

## Step-2 Create cron job:

Open crontab

```bash
crontab -e
```

Every 2 Months, 1st Day at 5:00 AM:

```bash
0 5 1 */2 * sudo <docker path location> compose -f <docker-compose.yaml file> up certbot
```

Daily at Midnight:

```bash
0 0 * * * sudo <docker path location> compose -f <docker-compose.yaml file> up certbot
```

## Step-3 Check cron status:

```bash
systemctl status cron
```

# Reference:

[Programonaut: Setup SSL with Docker, NGINX, and Lets Encrypt](https://www.programonaut.com/setup-ssl-with-docker-nginx-and-lets-encrypt/)
