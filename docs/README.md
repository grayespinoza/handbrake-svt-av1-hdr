# HandBrake-SVT-AV1-HDR

## Installation

### Arch Linux

Install from the
[Arch User Repository](https://aur.archlinux.org/packages/handbrake-svt-av1-hdr).
For example, using the [paru](https://github.com/morganamilo/paru) AUR helper:

```shell
paru -S handbrake-svt-av1-hdr
```

### Docker

Run as a [web-accessible container](https://github.com/grayespinoza/docker-handbrake-svt-av1-hdr):

#### Using `docker-compose`:

```yaml
---
services:
  handbrake-web:
    image: grayespinoza/handbrake-svt-av1-hdr:v1.11.2-svtav1hdr.cfb4e17
    container_name: handbrake-web
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Etc/UTC
    volumes:
      - /path/to/config:/config
    ports:
      - 3000:3000
      - 3001:3001
    shm_size: 1gb
    restart: unless-stopped
```

#### Using `docker run`:

```shell
docker run -d \
  --name=handbrake-web \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -v /path/to/config:/config \
  -p 3000:3000 \
  -p 3001:3001 \
  --shm-size="1gb" \
  --restart unless-stopped \
  grayespinoza/handbrake-svt-av1-hdr:v1.11.2-svtav1hdr.cfb4e17
```

## Reporting Issues

Please use [GitHub Issues](https://github.com/grayespinoza/handbrake-svt-av1-hdr/issues) to report bugs, crashes, and other issues.
