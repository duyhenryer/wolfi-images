# Shell Image

> Lightweight shell environment with essential tools built on Wolfi OS with zero known CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duyhenryer/wolfi-images/shell:latest         | latest       |
| ghcr.io/duyhenryer/wolfi-images/shell:latest-dev     | latest-dev   |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Essential shell tools (bash, curl, jq, yq) | Debugging, scripting, automation |
| `dev` | Extended toolset with development utilities | Development, troubleshooting, CI/CD |

## 🛠️ Included Tools

- **Shell**: `bash`, `sh`
- **Network**: `curl`, `wget`, `netcat`
- **Text Processing**: `jq`, `yq`, `grep`, `sed`, `awk`
- **System**: `ps`, `top`, `df`, `du`
- **Dev Tools** (in dev variant): `git`, `vim`, `nano`

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duyhenryer/wolfi-images/shell:latest

# Once available, run interactive shell
docker run --rm -it ghcr.io/duyhenryer/wolfi-images/shell:latest

# Run shell script
docker run --rm -v $(pwd):/scripts -w /scripts \
  ghcr.io/duyhenryer/wolfi-images/shell:latest bash script.sh
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duyhenryer/wolfi-images/shell:latest \
  --certificate-identity-regexp="https://github.com/duyhenryer/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```
