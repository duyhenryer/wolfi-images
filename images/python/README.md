# Python Image

> Minimal, secure Python runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags
| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duynhlab/wolfi-images/python:latest         | latest       |
| ghcr.io/duynhlab/wolfi-images/python:latest-shell   | latest-shell |
| ghcr.io/duynhlab/wolfi-images/python:latest-dev     | latest-dev   |
| ghcr.io/duynhlab/wolfi-images/python:3.13           | 3.13           |
| ghcr.io/duynhlab/wolfi-images/python:3.13-shell     | 3.13-shell     |
| ghcr.io/duynhlab/wolfi-images/python:3.13-dev       | 3.13-dev       |
| ghcr.io/duynhlab/wolfi-images/python:3.12           | 3.12           |
| ghcr.io/duynhlab/wolfi-images/python:3.12-shell     | 3.12-shell     |
| ghcr.io/duynhlab/wolfi-images/python:3.12-dev       | 3.12-dev       |
| ghcr.io/duynhlab/wolfi-images/python:3.11           | 3.11           |
| ghcr.io/duynhlab/wolfi-images/python:3.11-shell     | 3.11-shell     |
| ghcr.io/duynhlab/wolfi-images/python:3.11-dev       | 3.11-dev       |


## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Development, debugging, building |
| `shell` | Interactive shell with utilities | Debugging, troubleshooting |


## 📊 Image Info

```bash
# Check Python version
docker run --rm ghcr.io/duynhlab/wolfi-images/python:3.12 --version

# Check installed packages (dev variant)
docker run --rm ghcr.io/duynhlab/wolfi-images/python:3.12-dev -m pip list
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duynhlab/wolfi-images/python:3.12 \
  --certificate-identity-regexp="https://github.com/duynhlab/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/python:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/python@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/python:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/python:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/python:latest --fail-on high
```

Example output for a clean image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
