# Obsidian Container

Runs the Obsidian container with essential environment variables and port mapping.

```bash
docker run -d \
  --name obsidian \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 3000:3000 \
  -p 3001:3001 \
  --restart unless-stopped \
  lscr.io/linuxserver/obsidian:latest
