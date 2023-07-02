docker exec lb-server ln -s /etc/nginx/conf.d/sites-available/iot.pipigendut.tech.conf /etc/nginx/conf.d/sites-enabled/iot.pipigendut.tech.conf


docker exec lb-server nginx -t
docker exec lb-server service nginx reload
### Generate Certs
```bash
docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d mqtt.pipigendut.tech
docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d pipigendut.tech
```

### Renewing Certs
```bash
docker compose run --rm certbot renew
```

### Running
```bash
docker compose up -d
```

### Reference
https://mindsers.blog/post/https-using-nginx-certbot-docker/