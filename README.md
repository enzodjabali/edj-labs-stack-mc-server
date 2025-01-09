# Stack MC Server

![Uptime Kuma Badge](https://uptime-kuma.edj-labs.com/api/badge/36/status)

Note: <i>This stack uses Traefik. If you are willing to deploy Crafty using simply docker compose, check out `docker-compose` branch of this reposiroty.</i>

1. Change the values of `traefik.http.routers.portainer.rule` and `traefik.http.routers.portainer-http.rule` in docker-compose.yml


2. Deploy the stack using Docker Swarm:

```
docker stack deploy -c docker-compose.yml mc-server
```

Access Portainer at: https://crafty.your-domain.com
