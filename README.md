# Docker openSUSE Leap Systemd

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
