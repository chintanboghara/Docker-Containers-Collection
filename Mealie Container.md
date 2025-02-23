# Mealie Container

Runs Mealie, a self-hosted recipe management platform for culinary enthusiasts.

```bash
docker run -d \
  --name mealie \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 9925:9925 \
  --restart unless-stopped \
  ghcr.io/hay-kot/mealie:latest
