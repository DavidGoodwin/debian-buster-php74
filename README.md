# Public Docker image

## Features 

 * PHP 7.4 via deb.sury.org
 * Apache mod\_php
 
See also: https://hub.docker.com/r/davidgoodwin/docker-debian-php74/

## Building

```bash
docker build \
    --build-arg=http_proxy="http://192.168.86.66:3128" \
    --build-arg=https_proxy="http://192.168.86.66:3128" \
    --rm \
    -t davidgoodwin/debian-buster-php74:latest \
    -t davidgoodwin/debian-buster-php74:$(date +%F) \
    --pull \
    .



docker push davidgoodwin/debian-buster-php74:$(date +%F)
docker push davidgoodwin/debian-buster-php74:latest
```

