# LibreOffice Container

Runs a LibreOffice container using the LinuxServer image.

```bash
docker run -d \
  --name libreoffice \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 3000:3000 \
  -p 3001:3001 \
  --restart unless-stopped \
  lscr.io/linuxserver/libreoffice:latest
