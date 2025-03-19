# Scheduling Certbot Certificate Renewal

## Docker path location:

```bash
whereis docker
```

### Example output:

```bash
/usr/bin/docker
```

## Open crontab:

```bash
crontab -e
```

### Every 2 Months, 1st Day at 5:00 AM:

```bash
0 5 1 */2 * sudo /snap/bin/docker compose -f ./docker-compose.yaml up certbot
```

### Daily at Midnight:

```bash
0 0 * * * sudo /snap/bin/docker compose -f ./docker-compose.yaml up certbot
```

## Check cron status:

```bash
systemctl status cron
```
