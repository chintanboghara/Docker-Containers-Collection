# Ombi Container

Ombi is a media request system that integrates with media servers to allow users to request new content. While popular within media server circles, it’s still a niche solution outside that community.

```bash
docker run -d \
  --name ombi \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 3579:3579 \
  --restart unless-stopped \
  lscr.io/linuxserver/ombi:latest
