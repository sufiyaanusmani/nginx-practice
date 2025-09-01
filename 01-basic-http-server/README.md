# 01 - Basic HTTP Server (nginx)

This example shows a minimal static HTTP server using nginx inside Docker.

What’s included

- `Dockerfile` - builds an nginx image with a custom `nginx.conf` and static site.
- `docker-compose.yml` - convenience file to build and run the container (exposes host port 8080).
- `nginx.conf` - minimal nginx configuration with a `/health` endpoint.
- `site/` - simple static site (index, styles, 404).

Run locally

Build and run using Docker Compose:

```bash
docker compose up --build
```

Open http://localhost:8080 in your browser. Health check: http://localhost:8080/health

Stopping

```bash
docker compose down
```

Notes

- The container exposes port 80 and the compose file maps it to host `8080`.
- This is intentionally small and meant for learning. Next steps: add TLS, virtual hosts, or reverse proxying.
