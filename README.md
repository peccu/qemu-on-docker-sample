# QEMU sample

https://github.com/qemus/qemu-docker

- setup in CLI

for alpine or so

```
doco run -it --rm --name qemu qemu
```

```
d kill qemu
doco up -d
```

- setup in GUI

for almalinux or so

```
doco up
```

open http://0.0.0.0:8006

- ssh

```
# is in build/Dockerfile
# d exec -it qemu bash -c 'apt update && apt install -y openssh-client'
d exec -it qemu bash -c 'ssh root@20.20.20.21'
```

- mount volume

```
drunit vol --entrypoint sh -v qemu-on-docker-sample_storage:/storage -w /storage alpine
```
