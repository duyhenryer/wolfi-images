# Python Image

> Minimal, secure Python runtime built on Wolfi OS with zero known CVEs

## 🏷️ Available Tags
| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/python:latest         | latest       |
| ghcr.io/duyhenryer/wolfi-images/python:latest-shell   | latest-shell |
| ghcr.io/duyhenryer/wolfi-images/python:latest-dev     | latest-dev   |
| ghcr.io/duyhenryer/wolfi-images/python:3.12           | 3.12           |
| ghcr.io/duyhenryer/wolfi-images/python:3.12-shell     | 3.12-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.12-dev       | 3.12-dev       |
| ghcr.io/duyhenryer/wolfi-images/python:3.11           | 3.11           |
| ghcr.io/duyhenryer/wolfi-images/python:3.11-shell     | 3.11-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.11-dev       | 3.11-dev       |
| ghcr.io/duyhenryer/wolfi-images/python:3.10           | 3.10           |
| ghcr.io/duyhenryer/wolfi-images/python:3.10-shell     | 3.10-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.10-dev       | 3.10-dev       |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Development, debugging, building |
| `shell` | Interactive shell with utilities | Debugging, troubleshooting |


## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duyhenryer/wolfi-images/python:3.12

# Once available, check Python version
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:3.12 python --version

# Check installed packages
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:3.12-dev python -m pip list
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duyhenryer/wolfi-images/python:3.12 \
  --certificate-identity-regexp="https://github.com/duyhenryer/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```
