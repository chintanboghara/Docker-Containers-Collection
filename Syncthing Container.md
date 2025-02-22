# Syncthing Container

Syncthing provides secure, decentralized file synchronization between devices. This container is ideal for users looking for continuous file syncing.

```bash
docker run -d \
  --name syncthing \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 8384:8384 \
  -p 22000:22000 \
  -p 21027:21027/udp \
  --restart unless-stopped \
  lscr.io/linuxserver/syncthing:latest
