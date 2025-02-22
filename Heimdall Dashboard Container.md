# Heimdall Dashboard Container

Heimdall is a dashboard that centralizes access to your web applications and services. It’s a niche tool for users who want a custom portal for self-hosted apps.

```bash
docker run -d \
  --name heimdall \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 80:80 \
  --restart unless-stopped \
  lscr.io/linuxserver/heimdall:latest
