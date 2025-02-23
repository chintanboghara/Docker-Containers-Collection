# Ubooquity Container

Runs Ubooquity, a lightweight document and comic server for personal libraries.

```bash
docker run -d \
  --name ubooquity \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 2202:2202 \
  --restart unless-stopped \
  lscr.io/linuxserver/ubooquity:latest
