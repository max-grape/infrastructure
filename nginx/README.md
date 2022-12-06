# Nginx

## Obtain a certificate

```
docker run --rm -i -v letsencrypt:/etc/letsencrypt certbot/certbot:v2.0.0 certonly \
    --rsa-key-size 4096 \
    --agree-tos \
    --webroot \
    --webroot-path /etc/letsencrypt \
    -n \
    -m max.grape.box@gmail.com \
    -d dev.keyboard.dmska.ru
```

## List certificates

```
docker run --rm -i -v letsencrypt:/etc/letsencrypt certbot/certbot:v2.0.0 certificates
```

## Delete a certificate
```
docker run --rm -i -v letsencrypt:/etc/letsencrypt certbot/certbot:v2.0.0 delete -n --cert-name dev.keyboard.dmska.ru
```

## Renew certificates
```
docker run --rm -i -v letsencrypt:/etc/letsencrypt certbot/certbot:v2.0.0 renew
```
