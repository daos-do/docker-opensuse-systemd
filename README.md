# Docker openSUSE Leap Systemd

[![docker build](https://github.com/daos-do/docker-centos-systemd/workflows/docker%20build/badge.svg?branch=master)](https://hub.docker.com/repository/docker/daosdo/centos-systemd)

openSUSE Leap image that has systemd enabled.

## Branches

Each branch in the repository is used for building a specific version.

| Branch | openSUSE Leap Version | FROM Docker image tag |
| ------ | --------------------- | --------------------- |
| master | latest (15.2)         | latest                |
| 15.2   | 15.2                  | 15.2                  |
| 15.1   | 15.1                  | 15.1                  |

## Usage

### Run it

```
docker run -d \
  -- tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name daosd-opensuse-systemd \
  daosdo/opensuse-systemd:latest
```

Adding `--tty` allocates a pseudo-TTY and enables color in the logs when
running `docker logs`.

### Enter it

```
docker exec -it daosd-opensuse-systemd /bin/bash
```

### Remove it

```
docker rm -f daosd-opensuse-systemd
```
