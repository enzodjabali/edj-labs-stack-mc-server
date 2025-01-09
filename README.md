# Stack Swarm: MC Server

![Uptime Kuma Badge](https://uptime-kuma.edj-labs.com/api/badge/36/status)

Note: <i>This stack uses Traefik. If you are willing to deploy Crafty using simply docker compose, check out `docker-compose` branch of this repository.</i>

1. Change the value of `traefik.http.routers.crafty` in docker-compose.yml.

2. Because Crafty uses a self-signed certificate, add the insecureSkipVerify parameter to your `traefik.yml` config file and restart your traefik stack:

```
serversTransport:
  insecureSkipVerify: true
```

3. Deploy the stack using Docker Swarm:

```
docker stack deploy -c docker-compose.yml mc-server
```

Access Crafty at: https://crafty.your-domain.com
