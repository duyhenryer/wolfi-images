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
# Check nginx version
docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duyhenryer/wolfi-images/nginx:1.29 -v

# Test nginx configuration
docker run --rm -v $(pwd)/nginx.conf:/etc/nginx/nginx.conf \
  ghcr.io/duyhenryer/wolfi-images/nginx:1.29 nginx -t

# Run nginx server
docker run -d -p 8080:80 ghcr.io/duyhenryer/wolfi-images/nginx:1.29
```

