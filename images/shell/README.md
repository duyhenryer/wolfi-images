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
# Interactive shell
docker run --rm -it ghcr.io/duyhenryer/wolfi-images/shell:latest

# Run shell script
docker run --rm -v $(pwd):/scripts -w /scripts \
  ghcr.io/duyhenryer/wolfi-images/shell:latest bash script.sh

# Use as debugging sidecar
docker run --rm -it --network container:myapp \
  ghcr.io/duyhenryer/wolfi-images/shell:latest
```
