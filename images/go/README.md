# Go Image

> Fast and efficient Go runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duynhlab/wolfi-images/go:latest            | latest       |
| ghcr.io/duynhlab/wolfi-images/go:latest-dev        | latest-dev   |
| ghcr.io/duynhlab/wolfi-images/go:latest-shell      | latest-shell |
| ghcr.io/duynhlab/wolfi-images/go:1.26              | 1.26         |
| ghcr.io/duynhlab/wolfi-images/go:1.26-dev          | 1.26-dev     |
| ghcr.io/duynhlab/wolfi-images/go:1.26-shell        | 1.26-shell   |
| ghcr.io/duynhlab/wolfi-images/go:1.25              | 1.25         |
| ghcr.io/duynhlab/wolfi-images/go:1.25-dev          | 1.25-dev     |
| ghcr.io/duynhlab/wolfi-images/go:1.25-shell        | 1.25-shell   |
| ghcr.io/duynhlab/wolfi-images/go:1.24              | 1.24         |
| ghcr.io/duynhlab/wolfi-images/go:1.24-dev          | 1.24-dev     |
| ghcr.io/duynhlab/wolfi-images/go:1.24-shell        | 1.24-shell   |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Runtime, production deployments |
| `dev` | Development tools included | Building, testing, debugging |
| `shell` | Interactive shell with utilities | Development, troubleshooting |

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duynhlab/wolfi-images/go:latest

# Once available, check Go version
docker run --rm ghcr.io/duynhlab/wolfi-images/go:latest go version

# Build and run Go application
docker run --rm -v $(pwd):/app -w /app \
  ghcr.io/duynhlab/wolfi-images/go:latest-dev go run main.go
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duynhlab/wolfi-images/go:latest \
  --certificate-identity-regexp="https://github.com/duynhlab/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/go:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/go@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/go:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/go:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/go:latest --fail-on high
```

Expected result for a freshly built image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
