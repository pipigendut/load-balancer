### Running

Setup cerbot
1. commented nginx conf for ssl
2. RUN
```bash
docker compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ -d pipigendut.tech
docker compose run --rm certbot certonly --standalone --preferred-challenges http -d pipigendut.tech
```
3. uncommented nginx conf for ssl
4. RUN
```bash
docker-compose up -d