# SearxNG Container

Runs SearxNG, a privacy-respecting metasearch engine aggregating multiple search engines.

```bash
docker run -d \
  --name searxng \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -p 8888:8080 \
  --restart unless-stopped \
  ghcr.io/searxng/searxng:latest
