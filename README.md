### Generate Certs
```bash
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d iot.pipigendut.tech
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d pipigendut.tech
```

### Renewing Certs
```bash
docker-compose run --rm certbot renew
```

### Running
```bash
docker-compose up -d
```

### Reference
https://mindsers.blog/post/https-using-nginx-certbot-docker/