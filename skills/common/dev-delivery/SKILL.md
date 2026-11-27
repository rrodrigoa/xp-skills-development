---
name: dev-delivery
description: "Create project scaffolds, packaging, dependency management, CI, releases, versioning and reproducible development workflows."
---
# Delivery

Inspect existing build and support policy. Use the existing build manifest, conventional source layout, declared supported runtime versions and reproducible dependencies. Test the installed distribution, not just source imports. Configure least-privilege CI and protected releases. Verify build artifacts and report missing infrastructure rather than inventing deployment success.

## Reference selector
Read only relevant files from this list.

- [Project layout and build metadata](references/project-layout.md) — New library, tool or service.
- [Packaging and public distributions](references/packaging.md) — Publishing reusable library or CLI.
- [Dependency management and reproducibility](references/dependencies.md) — Adding dependencies or deploying.
- [Static analysis and quality toolchain](references/quality-toolchain.md) — Standardizing local and CI checks.
- [Continuous integration](references/ci.md) — Pull request verification and releases.
- [Versioning and releases](references/release.md) — Publishing artifact or breaking change.
- [README, docs and examples](references/documentation.md) — New feature or API change.
- [PR review and definition of done](references/code-review.md) — Before handing work back or merging.

For protected merge/release recommendations use `dev-quality-gates`; use `dev-governance` for project standards and exception approvals. The guidance package includes no CI workflow or build scripts.
