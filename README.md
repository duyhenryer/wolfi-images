# 🐺 Wolfi Images Collection

> Minimal, secure, and distroless container images built on [Wolfi OS](https://wolfi.dev) 🔒

## 🚀 Available Images

| 🏷️ Image Name | 📦 Pull Command |
|---------------|----------------|
| [**python**](./images/python/) | `docker pull ghcr.io/duynhlab/wolfi-images/python` |
| [**node**](./images/node/) | `docker pull ghcr.io/duynhlab/wolfi-images/node` |
| [**go**](./images/go/) | `docker pull ghcr.io/duynhlab/wolfi-images/go` |
| [**nginx**](./images/nginx/) | `docker pull ghcr.io/duynhlab/wolfi-images/nginx` |
| [**shell**](./images/shell/) | `docker pull ghcr.io/duynhlab/wolfi-images/shell` |

## ✨ Features

- 🔒 **Security First**: Built on Wolfi OS with minimal CVEs
- 📦 **Minimal Size**: Distroless images with only essential components
- 🏗️ **Multi-Architecture**: Supports both `amd64` and `arm64`
- 🔐 **Signed Images**: All images are signed with Sigstore/Cosign
- 📋 **SBOM Included**: Software Bill of Materials for transparency
- 🔄 **Auto-Updated**: Automated builds with latest security patches

## 🎯 Quick Start

```bash
# Python version
docker run --rm ghcr.io/duynhlab/wolfi-images/python:latest --version

# Node version  
docker run --rm ghcr.io/duynhlab/wolfi-images/node:latest --version

# Nginx version
docker run ghcr.io/duynhlab/wolfi-images/nginx:latest -version

# Go version
docker run ghcr.io/duynhlab/wolfi-images/go:latest version
```