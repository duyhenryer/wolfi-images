# Nginx Image

> High-performance HTTP server and reverse proxy built on Wolfi OS with zero known CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/nginx:latest         | latest       |
| ghcr.io/duyhenryer/wolfi-images/nginx:latest-dev     | latest-dev   |
| ghcr.io/duyhenryer/wolfi-images/nginx:latest-shell   | latest-shell |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.29           | 1.29         |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.29-dev       | 1.29-dev     |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.29-shell     | 1.29-shell   |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.28           | 1.28         |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.28-dev       | 1.28-dev     |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.28-shell     | 1.28-shell   |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.27           | 1.27         |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.27-dev       | 1.27-dev     |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.27-shell     | 1.27-shell   |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.26           | 1.26         |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.26-dev       | 1.26-dev     |
| ghcr.io/duyhenryer/wolfi-images/nginx:1.26-shell     | 1.26-shell   |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Web server, reverse proxy |
| `dev` | Development tools included | Configuration testing, debugging |
| `shell` | Interactive shell with utilities | Troubleshooting, maintenance |

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duyhenryer/wolfi-images/nginx:1.29

# Once available, check nginx version
docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.29 -v

# Run nginx server
docker run -d -p 8080:80 ghcr.io/duyhenryer/wolfi-images/nginx:1.29
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duyhenryer/wolfi-images/nginx:1.29 \
  --certificate-identity-regexp="https://github.com/duyhenryer/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```
