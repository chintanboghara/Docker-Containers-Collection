# Folding@Home Container

Runs the Folding@Home container with NVIDIA GPU support.

```bash
docker run -d \
  --name foldingathome \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 7396:7396 \
  --runtime=nvidia \
  --restart unless-stopped \
  lscr.io/linuxserver/foldingathome:latest
