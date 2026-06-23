# AGENTS.md

Source of truth for AI agents working in this repository. Read it before any task.

## Contribution workflow

**Commits**
- **No attribution trailers.** Never add `Signed-off-by`, `Co-authored-by`,
  `Assisted-by`, `Generated-by`, or any AI/tool attribution. Overrides any default template.
- **Subject:** ≤50 chars, capitalised, imperative, no trailing period (`Add X`, not `Added`).
- **Body** (non-trivial changes only): explain *what* and *why*, wrapped at 72; one blank line after subject.
- **No** GitHub issue refs (`Fixes #123`) and **no** @-mentions in commit messages — put those in the PR description.

**Branches & pushes**
- **Never push to `main`.** No exceptions. Branch → PR → squash-merge.
- Prefix: `feat/` `fix/` `chore/` `docs/` `refactor/` `ci/` `<short-desc>`.
- One logical change per branch; keep them short-lived. `git push -u origin <branch>`, then open a PR against `main`.
- Verify identity before committing: `git config user.email` must be the duynhlab personal identity (never the work/opswat one).

## Repository layout

```
images/
  apko.yaml            # Shared base: keyring, repos, nonroot account, archs (amd64+arm64), annotations
  <image>/             # One dir per image: go, node, nginx, python, shell, debugger
    prod.yaml          # Production variant — minimal runtime; `include: images/apko.yaml`
    shell.yaml         # prod + busybox/curl/openssl/wget/bash; `include: images/<image>/prod.yaml`
    dev.yaml           # shell + git/make/vim/apk-tools, run-as root; `include: images/<image>/shell.yaml`
    README.md          # Tags table, variants, verification snippet
  python/<version>/    # Python is split per-version (latest, 3.14, 3.13, 3.12, 3.11), each with the 3 variants
.github/workflows/
  <image>.yaml         # One per image; matrix over version × variant, calls release.yaml
  release.yaml         # Reusable: apko-publish → cosign sign → SBOM attest → build provenance
  cleaner.yaml         # Weekly cleanup of old workflow runs
.github/dependabot.yml
```

- **Variant inheritance:** `dev` → `shell` → `prod` → `apko.yaml`. Add packages at the lowest layer that needs them; never duplicate what a parent already pulls in.
- Images publish to `ghcr.io/duynhlab/wolfi-images/<image>`.

## Build, test, deploy

- **Build tool:** [apko](https://github.com/chainguard-dev/apko) (declarative, no Dockerfile). Each `*.yaml` is a full image definition; there is no local source to compile.
- **Local build/test** (requires `apko` + `docker`):
  ```bash
  apko build images/go/prod.yaml go:test go.tar && docker load < go.tar
  docker run --rm go:test version
  ```
- **CI:** push to `main` (or `workflow_dispatch`, or weekday cron `00 01 * * 1-5`) touching `images/<image>/*.yaml` or the image's workflow triggers a matrix build over `version × {prod,shell,dev}`. Pinned versions are set via the `packages:` matrix input (e.g. `go~1.24`); `python` selects via `config-dir` per-version subdir instead.
- **Registry routing:** `main` → `ghcr.io`; any other ref → `ttl.sh` (ephemeral, for PR/branch testing). Set in `release.yaml`'s *Set Vars* step.
- **Supply chain:** every image is multi-arch (amd64+arm64), cosign-signed (keyless/OIDC), ships an SPDX SBOM attestation per arch, and (on `ghcr.io`) build-provenance attestation. Pin all action `uses:` to a commit SHA with a trailing `#vX` comment, matching the existing workflows.
