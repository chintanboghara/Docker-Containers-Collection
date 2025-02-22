# Shairport Sync Container

Shairport Sync is an AirPlay audio player that enables streaming from Apple devices. This container is useful for home audio setups.

```bash
docker run -d \
  --name shairport-sync \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 5000:5000 \
  --restart unless-stopped \
  lscr.io/linuxserver/shairport-sync:latest
