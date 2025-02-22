# Calibre-Web Container

Calibre-Web offers a web-based interface for managing your ebook library. It’s a niche solution for ebook enthusiasts.

```bash
docker run -d \
  --name calibre-web \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 8083:8083 \
  --restart unless-stopped \
  lscr.io/linuxserver/calibre-web:latest
