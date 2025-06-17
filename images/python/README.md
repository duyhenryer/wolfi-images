# Python Image

## Available Tags
| 📌 Version    | ⬇️ Pull URL                               |
| ------------ | ------------------------------------------- |
| latest       | ghcr.io/duyhenryer/wolfi-images/python:latest       |
| latest-shell | ghcr.io/duyhenryer/wolfi-images/python:latest-shell |
| latest-dev   | ghcr.io/duyhenryer/wolfi-images/python:latest-dev   |
| 3.12           | ghcr.io/duyhenryer/wolfi-images/python:3.12           |
| 3.12-shell     | ghcr.io/duyhenryer/wolfi-images/python:3.12-shell     |
| 3.12-dev       | ghcr.io/duyhenryer/wolfi-images/python:3.12-dev       |
| 3.11           | ghcr.io/duyhenryer/wolfi-images/python:3.11           |
| 3.11-shell     | ghcr.io/duyhenryer/wolfi-images/python:3.11-shell     |
| 3.11-dev       | ghcr.io/duyhenryer/wolfi-images/python:3.11-dev       |
| 3.10           | ghcr.io/duyhenryer/wolfi-images/python:3.10           |
| 3.10-shell     | ghcr.io/duyhenryer/wolfi-images/python:3.10-shell     |
| 3.10-dev       | ghcr.io/duyhenryer/wolfi-images/python:3.10-dev       |

## Variants

- `prod`: Production image with minimal packages
- `dev`: Development image with additional tools
- `shell`: Shell image with bash and basic tools

## Usage

```bash
# Pull the image
docker pull ghcr.io/duyhenryer/wolfi-images/python:latest

# Run Python
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:latest python --version

# Run with shell
docker run --rm -it ghcr.io/duyhenryer/wolfi-images/python:latest-shell
```