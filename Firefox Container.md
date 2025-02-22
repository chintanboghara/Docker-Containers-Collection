# Firefox Container

Runs a Firefox container from the LinuxServer image with GUI support and appropriate shared memory settings.

```bash
docker run -d \
  --name firefox \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -e FIREFOX_CLI=https://x.com/ \
  -p 3000:3000 \
  -p 3001:3001 \
  --shm-size="1g" \
  --restart unless-stopped \
  lscr.io/linuxserver/firefox:latest
