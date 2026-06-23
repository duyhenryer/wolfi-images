# Nginx Image

> High-performance HTTP server and reverse proxy built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duynhlab/wolfi-images/nginx:latest         | latest       |
| ghcr.io/duynhlab/wolfi-images/nginx:latest-dev     | latest-dev   |
| ghcr.io/duynhlab/wolfi-images/nginx:latest-shell   | latest-shell |
| ghcr.io/duynhlab/wolfi-images/nginx:1.29           | 1.29         |
| ghcr.io/duynhlab/wolfi-images/nginx:1.29-dev       | 1.29-dev     |
| ghcr.io/duynhlab/wolfi-images/nginx:1.29-shell     | 1.29-shell   |
| ghcr.io/duynhlab/wolfi-images/nginx:1.28           | 1.28         |
| ghcr.io/duynhlab/wolfi-images/nginx:1.28-dev       | 1.28-dev     |
| ghcr.io/duynhlab/wolfi-images/nginx:1.28-shell     | 1.28-shell   |
| ghcr.io/duynhlab/wolfi-images/nginx:1.27           | 1.27         |
| ghcr.io/duynhlab/wolfi-images/nginx:1.27-dev       | 1.27-dev     |
| ghcr.io/duynhlab/wolfi-images/nginx:1.27-shell     | 1.27-shell   |
| ghcr.io/duynhlab/wolfi-images/nginx:1.26           | 1.26         |
| ghcr.io/duynhlab/wolfi-images/nginx:1.26-dev       | 1.26-dev     |
| ghcr.io/duynhlab/wolfi-images/nginx:1.26-shell     | 1.26-shell   |

## 📦 Variants

| Variant | Description | Use Case |
|---------|-------------|----------|
| `prod` | Production-ready with minimal packages | Web server, reverse proxy |
| `dev` | Development tools included | Configuration testing, debugging |
| `shell` | Interactive shell with utilities | Troubleshooting, maintenance |

## 📊 Image Info

```bash
# Check if image is available
docker manifest inspect ghcr.io/duynhlab/wolfi-images/nginx:1.29

# Once available, check nginx version
docker run --rm --entrypoint /usr/sbin/nginx ghcr.io/duynhlab/wolfi-images/nginx:1.29 -version
```

## 🔐 Image Verification

All images are signed with Sigstore. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duynhlab/wolfi-images/nginx:1.29 \
  --certificate-identity-regexp="https://github.com/duynhlab/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/nginx:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/nginx@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/nginx:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/nginx:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/nginx:latest --fail-on high
```

Expected result for a freshly built image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
