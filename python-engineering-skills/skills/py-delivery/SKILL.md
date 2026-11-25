---
name: py-delivery
description: "Create Python project scaffolds, packaging, dependency management, CI, releases, versioning and reproducible development workflows."
---
# Python Delivery

Inspect existing build and support policy. Use pyproject.toml, src layout when appropriate, declared supported Python versions and reproducible dependencies. Test the installed distribution, not just source imports. Configure least-privilege CI and protected releases. Verify build artifacts and report missing infrastructure rather than inventing deployment success.

## Reference selector
Read only relevant files from this list.

- [Project layout and pyproject](references/project-layout.md) — New library, tool or service.
- [Python packaging and public distributions](references/packaging.md) — Publishing reusable library or CLI.
- [Dependency management and reproducibility](references/dependencies.md) — Adding dependencies or deploying.
- [Ruff, type checking and quality gates](references/quality-toolchain.md) — Standardizing local and CI checks.
- [Continuous integration](references/ci.md) — Pull request verification and releases.
- [Versioning and releases](references/release.md) — Publishing artifact or breaking change.
- [README, docs and examples](references/documentation.md) — New feature or API change.
- [PR review and definition of done](references/code-review.md) — Before handing work back or merging.

For protected merge/release recommendations use `py-quality-gates`; use `py-governance` for project standards and exception approvals. The guidance package includes no CI workflow or build scripts.
