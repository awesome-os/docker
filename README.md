# just-js docker images and container builds

## building debian docker image

```bash
make debian
```

## building distroless docker image

```bash
make distroless
```

## running in gvisor

```bash
docker export $(docker create hello-world) | tar -xf - -C rootfs
cp just rootfs/
runsc spec -- /just
sudo runsc run just
```

## Quick Start (Windows / Linux / macOS)

```sh
# Clone & enter repository (all platforms)
git clone https://github.com/awesome-os/docker.git && cd docker
```
