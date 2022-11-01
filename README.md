# Minio Server

## Features

Minio Object storage

## Getting started

- Create new A DNS record for `minio.domain.com` and `minio-console.domain.com`

- Override `.env` configuration to match your domain name and buckets credentials:

```bash
vim .env
```

- Override the mail adress to resolve tls challenges in `traefik/traefik.toml`.

```bash
vim traefik/traefik.toml
```

- Prepare an empty acme.json and traefik.log (with the appropriate permissions) by running:

```bash
touch traefik/acme.json
sudo chmod 600 traefik/acme.json
touch traefik/traefik.log
sudo chmod 600 traefik/traefik.log
```

Create external network by running:

```bash
docker network create traefik_public
```

Launch the containers:

```bash
docker-compose up -d
```
