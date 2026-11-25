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

## Quick Install & Run (Windows / Linux / macOS)

```sh
# Install / hydrate from v11 CAS via holo-pm
holo-pm install repository://github.com/awesome-os/docker@main

# Or project & run directly via holo-project (0-byte hardlink)
holo-project "project://cpp/docker?from=repository://github.com/awesome-os/docker@main"
```
