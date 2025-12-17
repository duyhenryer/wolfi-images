# Go Image

> Fast and efficient Go runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/go:latest            | latest       |
| ghcr.io/duyhenryer/wolfi-images/go:latest-dev        | latest-dev   |
| ghcr.io/duyhenryer/wolfi-images/go:latest-shell      | latest-shell |
| ghcr.io/duyhenryer/wolfi-images/go:1.25              | 1.25         |
| ghcr.io/duyhenryer/wolfi-images/go:1.25-dev          | 1.25-dev     |
| ghcr.io/duyhenryer/wolfi-images/go:1.25-shell        | 1.25-shell   |
| ghcr.io/duyhenryer/wolfi-images/go:1.24              | 1.24         |
| ghcr.io/duyhenryer/wolfi-images/go:1.24-dev          | 1.24-dev     |
| ghcr.io/duyhenryer/wolfi-images/go:1.24-shell        | 1.24-shell   |
| ghcr.io/duyhenryer/wolfi-images/go:1.23              | 1.23         |
| ghcr.io/duyhenryer/wolfi-images/go:1.23-dev          | 1.23-dev     |
| ghcr.io/duyhenryer/wolfi-images/go:1.23-shell        | 1.23-shell   |
| ghcr.io/duyhenryer/wolfi-images/go:1.22              | 1.22         |
| ghcr.io/duyhenryer/wolfi-images/go:1.22-dev          | 1.22-dev     |
| ghcr.io/duyhenryer/wolfi-images/go:1.22-shell        | 1.22-shell   |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Building, testing, debugging |
| `shell` | Interactive shell with utilities | Development, troubleshooting |

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duyhenryer/wolfi-images/go:latest

# Once available, check Go version
docker run --rm ghcr.io/duyhenryer/wolfi-images/go:latest go version

# Build and run Go application
docker run --rm -v $(pwd):/app -w /app \
  ghcr.io/duyhenryer/wolfi-images/go:latest-dev go run main.go
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duyhenryer/wolfi-images/go:latest \
  --certificate-identity-regexp="https://github.com/duyhenryer/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```