# Debugger Image

> Fast and efficient Go runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| 📌 Version  | ⬇️ Pull URL                                         |
| ---------- | -------------------------------------------------- |
| latest     | ghcr.io/duyhenryer/wolfi-images/debugger:latest       |
| latest-dev | ghcr.io/duyhenryer/wolfi-images/debugger:latest-shell |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `latest` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Building, testing, debugging |

## 🔐 Image Verification

GitHub CLI ([gh](https://cli.github.com/)) can be used to retrieve the build provenance, which details the exact commit, workflow, and runner that produced the image:

- **Production image**

```shell
gh attestation verify \
  --owner duyhenryer \
  oci://ghcr.io/duyhenryer/wolfi-images/debugger:latest
```

- **Shell image**

```shell
gh attestation verify \
  --owner duyhenryer \
  oci://ghcr.io/duyhenryer/wolfi-images/debugger:latest-shell
```
