# Python Image

## Available Tags

| Tag | Description |
|-----|-------------|
| latest | Latest Python version |
| 3.12 | Python 3.12 |
| 3.11 | Python 3.11 |
| 3.10 | Python 3.10 |

## Variants

- `prod`: Production image with minimal packages
- `dev`: Development image with additional tools
- `shell`: Shell image with bash and basic tools

## Usage

```bash
# Pull the image
docker pull ghcr.io/duyhenryer/wolfi-images/python:latest

# Run Python
docker run --rm ghcr.io/duyhenryer/wolfi-images/python:latest python3 --version

# Run with shell
docker run --rm -it ghcr.io/duyhenryer/wolfi-images/python:latest-shell
```