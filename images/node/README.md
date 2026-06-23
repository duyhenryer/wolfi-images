# Node.js Image

> Modern JavaScript runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duynhlab/wolfi-images/node:latest          | latest       |
| ghcr.io/duynhlab/wolfi-images/node:latest-shell    | latest-shell |
| ghcr.io/duynhlab/wolfi-images/node:latest-dev      | latest-dev   |
| ghcr.io/duynhlab/wolfi-images/node:23              | 23           |
| ghcr.io/duynhlab/wolfi-images/node:23-shell        | 23-shell     |
| ghcr.io/duynhlab/wolfi-images/node:23-dev          | 23-dev       |
| ghcr.io/duynhlab/wolfi-images/node:22              | 22           |
| ghcr.io/duynhlab/wolfi-images/node:22-shell        | 22-shell     |
| ghcr.io/duynhlab/wolfi-images/node:22-dev          | 22-dev       |
| ghcr.io/duynhlab/wolfi-images/node:20              | 20           |
| ghcr.io/duynhlab/wolfi-images/node:20-shell        | 20-shell     |
| ghcr.io/duynhlab/wolfi-images/node:20-dev          | 20-dev       |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Building, testing, npm install |
| `shell` | Interactive shell with utilities | Development, troubleshooting |

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duynhlab/wolfi-images/node:latest

# Check Node.js version
docker run --rm ghcr.io/duynhlab/wolfi-images/node:latest --version
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duynhlab/wolfi-images/node:latest \
  --certificate-identity-regexp="https://github.com/duynhlab/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/node:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/node@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/node:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/node:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/node:latest --fail-on high
```

Example output for a clean image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
