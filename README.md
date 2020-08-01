# Docker openSUSE Leap Systemd

[![build status](https://img.shields.io/docker/cloud/build/daosdo/opensuse-systemd)](https://hub.docker.com/repository/docker/daosdo/opensuse-systemd)

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

```bash
docker run -d \
  -- tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name daosd-opensuse15.1-systemd \
  daosdo/opensuse-systemd:15.1
```

Adding `--tty` allocates a pseudo-TTY and enables color in the logs when
running `docker logs`.

### Enter it

```bash
docker exec -it daosd-opensuse15.1-systemd /bin/bash
```

### Remove it

```bash
docker rm -f daosd-opensuse15.1-systemd
```
