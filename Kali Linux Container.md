# Kali Linux Container

Runs a Kali Linux container with GPU device mapping and shared memory configuration.

```bash
docker run -d \
  --name kali-linux \
  --security-opt seccomp=unconfined \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -e SUBFOLDER=/ \
  -p 3000:3000 \
  -p 3001:3001 \
  --device /dev/dri:/dev/dri \
  --shm-size="1g" \
  --restart unless-stopped \
  lscr.io/linuxserver/kali-linux:latest
