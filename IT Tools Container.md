# IT Tools Container

This container provides a suite of IT tools for system diagnostics and management. It maps the container's port 80 to the host's port 8080.

```bash
docker run -d \
  --name it-tools \
  -p 8080:80 \
  -it corentinth/it-tools
