# AlmaLinux docker image
![Build](https://github.com/artem-shestakov/oraclelinux-docker/actions/workflows/Build/badge.svg)
Oreacle Linux image for ansible tests with systemd
>Based on [geerlingguy /
docker-centos8-ansible](https://github.com/geerlingguy/docker-centos8-ansible)
## How to
Add instance to `molecule.yml` file:
```yaml
...
platforms:
  - name: instance
    image: artemshestakov/almalinux-8-docker:latest
    volumes:
      - /sys/fs/cgroup:/sys/fs/cgroup:ro
    privileged: true
    pre_build_image: true
```