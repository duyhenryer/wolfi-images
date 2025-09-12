# Nginx
# Nginx

Minimal Wolfi-based nginx HTTP, reverse proxy, mail proxy, and a generic TCP/UDP proxy server

| 📌 Version    | ⬇️ Pull URL                                   |
| ------------ | -------------------------------------------- |
| latest       | ghcr.io/duyhenryer/wolfi-images/nginx:latest       |
| latest-dev   | ghcr.io/duyhenryer/wolfi-images/nginx:latest-dev   |
| latest-shell | ghcr.io/duyhenryer/wolfi-images/nginx:latest-shell |
| 1.29         | ghcr.io/duyhenryer/wolfi-images/nginx:1.29         |
| 1.29-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.29-dev     |
| 1.29-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.29-shell   |
| 1.28         | ghcr.io/duyhenryer/wolfi-images/nginx:1.28         |
| 1.28-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.28-dev     |
| 1.28-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.28-shell   |
| 1.27         | ghcr.io/duyhenryer/wolfi-images/nginx:1.27         |
| 1.27-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.27-dev     |
| 1.27-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell   |
| 1.26         | ghcr.io/duyhenryer/wolfi-images/nginx:1.26         |
| 1.26-dev     | ghcr.io/duyhenryer/wolfi-images/nginx:1.26-dev     |
| 1.26-shell   | ghcr.io/duyhenryer/wolfi-images/nginx:1.26-shell   |

## ✅ Check version
```sh
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.26 -v
nginx version: nginx/1.26.3
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.27 -v
nginx version: nginx/1.27.5
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.28 -v
nginx version: nginx/1.28.0
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.29 -v
nginx version: nginx/1.29.1
❯ docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.29-shell -v
nginx version: nginx/1.29.1
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

