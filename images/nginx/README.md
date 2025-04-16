# Nginx
# Nginx

Minimal Wolfi-based nginx HTTP, reverse proxy, mail proxy, and a generic TCP/UDP proxy server

| 📌 Version    | ⬇️ Pull URL                                   |
| ------------ | -------------------------------------------- |
| latest       | ghcr.io/duyhenryer/wolfi-images/nginx:latest       |
| latest-dev   | ghcr.io/duyhenryer/wolfi-images/nginx:latest-dev   |
| latest-shell | ghcr.io/duyhenryer/wolfi-images/nginx:latest-shell |
| 1.27         | ghcr.io/duyhenryer/wolfi-images/nginx:1.27         |
| 1.27-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.27-dev     |
| 1.27-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell   |
| 1.26         | ghcr.io/duyhenryer/wolfi-images/nginx:1.26         |
| 1.26-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.26-dev     |
| 1.26-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.26-shell   |
| 1.25         | ghcr.io/duyhenryer/wolfi-images/nginx:1.25         |
| 1.25-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.25-dev     |
| 1.25-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.25-shell   |

## ✅ Check version
```sh
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.25 -v
nginx version: nginx/1.25.5
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.26 -v
nginx version: nginx/1.26.3
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.27 -v
nginx version: nginx/1.27.4
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell -v
Unable to find image 'ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell' locally
1.27-shell: Pulling from duyhenryer/wolfi-images/nginx
5b8fa02f5d6e: Pull complete
Digest: sha256:21a945e39f25398ab31b8bd13830f037c46aaff0472d62a22719e48ce68ea496
Status: Downloaded newer image for ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell
nginx version: nginx/1.27.4
```

## ✅ Verify the Provenance

GitHub CLI ([gh](https://cli.github.com/)) can be used to retrieve the build provenance, which details the exact commit, workflow, and runner that produced the image:

- **Production image**

```shell
gh attestation verify \
  --owner duyhenryer \
  oci://ghcr.io/duyhenryer/wolfi-images/nginx:latest
```

- **Shell image**

```shell
gh attestation verify \
  --owner gitguardian \
  oci://ghcr.io/duyhenryer/wolfi-images/nginx:latest-shell
```

- **Dev image**

```shell
gh attestation verify \
  --owner gitguardian \
  oci://ghcr.io/duyhenryer/wolfi-images/nginx:latest-dev
```

