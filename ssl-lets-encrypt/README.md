This project test out how letsencrypt work together with nginx in docker context.

# Problems

- generate new certificates for http site

- migrate from http to https

- deploy https site in docker context

    1. start a host default nginx to help use certbot/certbot docker container generate new certs

    2. close host nginx, start app containers
