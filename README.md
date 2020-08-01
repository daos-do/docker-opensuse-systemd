# Docker openSUSE Leap Systemd

[![docker build](https://github.com/daos-do/docker-opensuse-systemd/workflows/docker%20build/badge.svg?branch=15.1)](https://hub.docker.com/repository/docker/daosdo/opensuse-systemd)

A Dockerfile for building openSUSE Leap images that have systemd enabled.

## Branches

Each branch in this git repository is used for building specific versions
of openSUSE Leap images.

The master branch contains the latest version.

|Branch |openSUSE Leap Version|FROM Docker image tag|
|-------|---------------------|---------------------|
|master |latest (15.2)        |latest               |
|15.2   |15.2                 |15.2                 |
|15.1   |15.1                 |15.1                 |

## Usage

### Run it

```
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name daosd-opensuse15.1-systemd \
  daosdo/opensuse-systemd:15.1
```

Adding `--tty` allocates a pseudo-TTY and enables color in the logs when
running `docker logs`.

### Enter it

```
docker exec -it daosd-opensuse15.1-systemd /bin/bash
```

### Remove it

```
docker rm -f daosd-opensuse15.1-systemd
```
