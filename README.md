# Kevin's Home Automation Setup

## Setup
Create the required docker networks

```bash
docker network create traefik && \
docker network create mqtt
```

### Docker: mqtt
Create the config file in `./data/mqtt/mosquitto.conf` with the following contents:
```conf
persistence true
persistence_location /mosquitto/data/
log_dest file /mosquitto/log/mosquitto.log
listener 1883
allow_anonymous true
```

### Docker: Traefik
Set the enviroment variables in `./docker/traefik/.env`.

Create an empty docker file at `./data/traefik/acme.json` and set the file permissions to `600`.
```bash
mkdir -p ./data/traefik/ && \
touch ./data/traefik/acme.json && \
chmod 600 ./data/traefik/acme.json
```
