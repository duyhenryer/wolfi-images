# 🐺 Wolfi Images Collection

> Minimal, secure, and distroless container images built on [Wolfi OS](https://wolfi.dev) 🔒

## 🚀 Available Images

| 🏷️ Image Name | 📦 Pull Command |
|---------------|----------------|
| [**python**](./images/python/) | `docker pull ghcr.io/duyhenryer/wolfi-images/python` |
| [**node**](./images/node/) | `docker pull ghcr.io/duyhenryer/wolfi-images/node` |
| [**go**](./images/go/) | `docker pull ghcr.io/duyhenryer/wolfi-images/go` |
| [**nginx**](./images/nginx/) | `docker pull ghcr.io/duyhenryer/wolfi-images/nginx` |
| [**shell**](./images/shell/) | `docker pull ghcr.io/duyhenryer/wolfi-images/shell` |

## ✨ Features

- 🔒 **Security First**: Built on Wolfi OS with no known CVEs
- 📦 **Minimal Size**: Distroless images with only essential components
- 🚀 **Multi-Architecture**: Supports both `amd64` and `arm64`
- 🔐 **Signed Images**: All images are signed with Sigstore/Cosign
- 📋 **SBOM Included**: Software Bill of Materials for transparency
- 🔄 **Auto-Updated**: Automated builds with latest security patches

## 🎯 Quick Start

```bash
# Python example
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:3.12 python --version

# Node.js example  
docker run --rm ghcr.io/duyhenryer/wolfi-images/node:latest node --version

# Nginx example
docker run -p 8080:80 ghcr.io/duyhenryer/wolfi-images/nginx:latest
```
