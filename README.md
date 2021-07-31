# Kevin's Home Automation Setup

## Setup
Create the required docker networks

```bash
docker network create traefik
```

#### Docker: Traefik
Set the enviroment variables in `./docker/traefik/.env`.

Create an empty docker file at `./data/traefik/acme.json` and set the file permissions to `600`.
```bash
mkdir -p ./data/traefik/ && \
touch ./data/traefik/acme.json && \
chmod 600 ./data/traefik/acme.json
```
