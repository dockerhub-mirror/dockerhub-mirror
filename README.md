# dockerhub-mirror

[![Sync Status](https://github.com/dockerhub-mirror/dockerhub-mirror/actions/workflows/mirror-images.yml/badge.svg)](https://github.com/dockerhub-mirror/dockerhub-mirror/actions/workflows/mirror-images.yml)

This repository **mirrors selected public images from Docker Hub to GitHub Container Registry (GHCR)**,
so you can pull them without depending on Docker Hub's availability or being subject to its rate limits.

> **NOTE:** The purpose of **dockerhub-mirror** is _not_ to mirror every image available on Docker Hub.
> Instead, this repository demonstrates how to mirror a **selected subset** of public images for convenience.
>
> If you require a custom or comprehensive mirror for your organization, you can **fork this repository**
> and run it within your own GitHub organization, adjusting the list of images and workflows to your needs.

## Where to Pull

All images live under the namespace `ghcr.io/dockerhub-mirrors`.
When an upstream image name contains a slash (i.e. includes an organisation as well as a repository),
the slash is replaced with a double underscore (`__`) to separate the upstream organisation and repository names.

| Upstream on Docker Hub              | Mirrored on GHCR
| ----------------------------------- | ----------------
| `alpine:3`                          | `ghcr.io/dockerhub-mirror/alpine:3`
| `alpine:latest`                     | `ghcr.io/dockerhub-mirror/alpine:latest`
| `bitnami/minideb:bookworm`          | `ghcr.io/dockerhub-mirror/bitnami__minideb:bookworm`
| `bitnami/minideb:latest`            | `ghcr.io/dockerhub-mirror/bitnami__minideb:latest`
| `busybox:1`                         | `ghcr.io/dockerhub-mirror/busybox:1`
| `busybox:latest`                    | `ghcr.io/dockerhub-mirror/busybox:latest`
| `busybox:stable`                    | `ghcr.io/dockerhub-mirror/busybox:stable`
| `busybox:stable-musl`               | `ghcr.io/dockerhub-mirror/busybox:stable-musl`
| `debian:bookworm`                   | `ghcr.io/dockerhub-mirror/debian:bookworm`
| `debian:bookworm-slim`              | `ghcr.io/dockerhub-mirror/debian:bookworm-slim`
| `debian:stable`                     | `ghcr.io/dockerhub-mirror/debian:stable`
| `debian:stable-slim`                | `ghcr.io/dockerhub-mirror/debian:stable-slim`
| `moby/buildkit:buildx-stable-1`     | `ghcr.io/dockerhub-mirror/buildkit:buildx-stable-1`
| `moby/buildkit:buildx-stable-1-rootless` | `ghcr.io/dockerhub-mirror/buildkit:buildx-stable-1-rootless`
| `moby/buildkit:latest`              | `ghcr.io/dockerhub-mirror/buildkit:latest`
| `moby/buildkit:rootless`            | `ghcr.io/dockerhub-mirror/buildkit:rootless`
| `node:current`                      | `ghcr.io/dockerhub-mirror/node:current`
| `node:current-slim`                 | `ghcr.io/dockerhub-mirror/node:current-slim`
| `node:lts`                          | `ghcr.io/dockerhub-mirror/node:lts`
| `node:lts-slim`                     | `ghcr.io/dockerhub-mirror/node:lts-slim`
| `registry:latest`                   | `ghcr.io/dockerhub-mirror/registry:latest`
| `multiarch/qemu-user-static:latest` | `ghcr.io/dockerhub-mirror/multiarch_qemu-user-static:latest`
| `tonistiigi/binfmt:latest`          | `ghcr.io/dockerhub-mirror/tonistiigi__binfmt:latest`

> **Example**
>
> ```bash
> docker pull ghcr.io/dockerhub-mirror/alpine:latest
> ```


## Legal Notice

* **Content License** – All content in this repository is dedicated to the public domain.
* **Licences** - Each docker image remains under its original upstream licence (GPL, Apache 2.0, BSD, etc.). We do **not** alter or re-license the contents.
* **Trademarks** - *Docker®, Alpine®, Debian®,* and all other trademarks are the property of their respective owners. This project is **not** affiliated with or endorsed by those projects.
* **Warranty** - Images are provided *“as is”* **without any warranty**. Use at your own risk.
* **Indemnification** - By using these images you agree to indemnify the maintainers against any claims arising from such use or redistribution.
