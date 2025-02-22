# Docker-OSX Container

Runs a Docker-OSX container with KVM virtualization and X11 socket mapping for GUI support.

```bash
docker run -it \
  --device /dev/kvm \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  --net=host \
  -e GENERATE-UNIQUE=true \
  -e MASTER_PLIST_URL=https://raw.githubusercontent.com/sickcodes/osx-serial-generator/master/config-custom.plist \
  seraphix/docker-osx:sonoma
