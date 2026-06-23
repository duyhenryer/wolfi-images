# Debugger Image

> Fast and efficient Go runtime built on Wolfi OS with minimal CVEs

## 🏷️ Available Tags

| 📌 Version  | ⬇️ Pull URL                                         |
| ---------- | -------------------------------------------------- |
| latest     | ghcr.io/duynhlab/wolfi-images/debugger:latest       |
| latest-dev | ghcr.io/duynhlab/wolfi-images/debugger:latest-shell |

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
  --owner duynhlab \
  oci://ghcr.io/duynhlab/wolfi-images/debugger:latest
```

- **Shell image**

```shell
gh attestation verify \
  --owner duynhlab \
  oci://ghcr.io/duynhlab/wolfi-images/debugger:latest-shell
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/debugger:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/debugger@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/debugger:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/debugger:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/debugger:latest --fail-on high
```

Expected result for a freshly built image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
