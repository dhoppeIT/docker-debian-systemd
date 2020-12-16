# Debian image including Systemd

This [Docker](https://www.docker.com) image can be used to test [Ansible](https://www.ansible.com) playbooks based on [Molecule](https://molecule.readthedocs.io).

## Supported tags

|Branch|Debian version|Docker image tag|
|------|--------------|----------------|
|master|10            |10              |
|9     |9             |9               |
|10    |10            |10              |

## Usage

### Start the container

```console
docker run \
  --cap-add SYS_ADMIN \
  --detach \
  --name debian-10 \
  --rm \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  dhoppeit/docker-debian-systemd:10
```

### Enter the container

```console
docker exec -it debian-10 bash
```

### Stop the container

```console
docker stop debian-10
```
