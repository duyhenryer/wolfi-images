# Shell Image

> Lightweight shell environment with essential tools built on Wolfi OS with zero known CVEs

## 🏷️ Available Tags

| ⬇️ Pull URL                                           | 📌 Version    |
| ----------------------------------------------------- | ------------ |
| ghcr.io/duynhlab/wolfi-images/shell:latest         | latest       |
| ghcr.io/duynhlab/wolfi-images/shell:latest-dev     | latest-dev   |

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
docker manifest inspect ghcr.io/duynhlab/wolfi-images/shell:latest

# Once available, run interactive shell
docker run --rm -it ghcr.io/duynhlab/wolfi-images/shell:latest bash
```

## 🔐 Image Verification
✅ ***Verify the Provenance***

GitHub CLI (`gh`) can be used to retrieve the build provenance, which details the exact commit, workflow, and runner that produced the image:
```sh
gh attestation verify \
  --owner duynhlab \
  oci://ghcr.io/duynhlab/wolfi-images/shell:latest-shell
```

✅ ***Verify the Image Signature***

All images are signed with `Sigstore`. Once images are published, verify authenticity:

```bash
# Verify image signature (after successful build)
cosign verify ghcr.io/duynhlab/wolfi-images/shell:latest \
  --certificate-identity-regexp="https://github.com/duynhlab/wolfi-images" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## 🛡️ Vulnerability Scanning

Built on Wolfi OS to keep CVEs near zero. Scan any tag yourself with [Grype](https://github.com/anchore/grype):

```bash
# Full scan — list all CVEs
grype ghcr.io/duynhlab/wolfi-images/shell:latest

# Pin to an immutable digest
grype ghcr.io/duynhlab/wolfi-images/shell@sha256:<digest>

# JSON output (CI integration)
grype ghcr.io/duynhlab/wolfi-images/shell:latest -o json

# Only vulnerabilities that have a fix available
grype ghcr.io/duynhlab/wolfi-images/shell:latest --only-fixed

# Fail (non-zero exit) on high/critical — use as a CI/CD gate
grype ghcr.io/duynhlab/wolfi-images/shell:latest --fail-on high
```

Expected result for a freshly built image:

```text
 ✔ Scanned for vulnerabilities     [0 vulnerability matches]
   └── by severity: 0 critical, 0 high, 0 medium, 0 low, 0 negligible
No vulnerabilities found
```

> CI scans every published image automatically and uploads results to the repo's **Security → Code scanning** tab.
