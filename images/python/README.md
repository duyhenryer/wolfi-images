# Python Image

> Minimal, secure Python runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags
| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/python:latest         | latest       |
| ghcr.io/duyhenryer/wolfi-images/python:latest-shell   | latest-shell |
| ghcr.io/duyhenryer/wolfi-images/python:latest-dev     | latest-dev   |
| ghcr.io/duyhenryer/wolfi-images/python:3.13           | 3.13           |
| ghcr.io/duyhenryer/wolfi-images/python:3.13-shell     | 3.13-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.13-dev       | 3.13-dev       |
| ghcr.io/duyhenryer/wolfi-images/python:3.12           | 3.12           |
| ghcr.io/duyhenryer/wolfi-images/python:3.12-shell     | 3.12-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.12-dev       | 3.12-dev       |
| ghcr.io/duyhenryer/wolfi-images/python:3.11           | 3.11           |
| ghcr.io/duyhenryer/wolfi-images/python:3.11-shell     | 3.11-shell     |
| ghcr.io/duyhenryer/wolfi-images/python:3.11-dev       | 3.11-dev       |


## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Development, debugging, building |
| `shell` | Interactive shell with utilities | Debugging, troubleshooting |


## 📊 Image Info

```bash
# Check Python version
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:3.12 --version

# Check installed packages (dev variant)
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:3.12-dev -m pip list
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duyhenryer/wolfi-images/python:3.12 \
  --certificate-identity-regexp="https://github.com/duyhenryer/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```
