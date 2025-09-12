# Node.js Image

> Modern JavaScript runtime built on Wolfi OS with zero known CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/node:latest          | latest       |
| ghcr.io/duyhenryer/wolfi-images/node:latest-shell    | latest-shell |
| ghcr.io/duyhenryer/wolfi-images/node:latest-dev      | latest-dev   |
| ghcr.io/duyhenryer/wolfi-images/node:23              | 23           |
| ghcr.io/duyhenryer/wolfi-images/node:23-shell        | 23-shell     |
| ghcr.io/duyhenryer/wolfi-images/node:23-dev          | 23-dev       |
| ghcr.io/duyhenryer/wolfi-images/node:22              | 22           |
| ghcr.io/duyhenryer/wolfi-images/node:22-shell        | 22-shell     |
| ghcr.io/duyhenryer/wolfi-images/node:22-dev          | 22-dev       |
| ghcr.io/duyhenryer/wolfi-images/node:20              | 20           |
| ghcr.io/duyhenryer/wolfi-images/node:20-shell        | 20-shell     |
| ghcr.io/duyhenryer/wolfi-images/node:20-dev          | 20-dev       |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Building, testing, npm install |
| `shell` | Interactive shell with utilities | Development, troubleshooting |

## 📊 Image Info

```bash
# Check Node.js version
docker run --rm ghcr.io/duyhenryer/wolfi-images/node:latest node --version

# Run Node.js application
docker run --rm -v $(pwd):/app -w /app \
  ghcr.io/duyhenryer/wolfi-images/node:22 node index.js

# Install dependencies and build
docker run --rm -v $(pwd):/app -w /app \
  ghcr.io/duyhenryer/wolfi-images/node:22-dev npm install && npm run build
```
