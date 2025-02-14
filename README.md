# Stack Swarm: MC Server

![Uptime Kuma Badge](https://uptime-kuma.edj-labs.com/api/badge/36/status)

Note: <i>This stack uses Traefik. If you are willing to deploy Crafty using simply docker compose, check out `docker-compose` branch of this repository.</i>

1. Change the value of `traefik.http.routers.crafty` in docker-compose.yml.

2. Because Crafty uses a self-signed certificate, add the insecureSkipVerify parameter to your `traefik.yml` config file and restart your traefik stack:

```yaml
serversTransport:
  insecureSkipVerify: true
```

3. Create the Crafty required directories:
```bash
mkdir -p /data/docker/crafty/backups
mkdir -p /data/docker/crafty/logs
mkdir -p /data/docker/crafty/servers
mkdir -p /data/docker/crafty/config
mkdir -p /data/docker/crafty/import
```

4. Deploy the stack using Docker Swarm:

```bash
docker stack deploy -c docker-compose.yml mc-server
```

Access Crafty at: https://crafty.your-domain.com
