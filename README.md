This documentation consists of:

1. [Generate Wallet Address](https://github.com/ValdryanIvandito/cardano-basic-transaction-guide/blob/main/generate-wallet-address-eng.md)
2. [Basic Transaction](https://github.com/ValdryanIvandito/cardano-basic-transaction-guide/blob/main/transaction-eng.md)
3. [Transaction with Metadata](https://github.com/ValdryanIvandito/cardano-basic-transaction-guide/blob/main/metadata-eng.md)



# References

1. 

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
