---
name: py-delivery
description: "Build and release Python projects; manage dependencies, compatibility, static checks and revision-bound evidence."
---
# Python Delivery

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-delivery and applicable dev-quality-gates. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Python project layout and pyproject](references/project-layout.md) — New or reorganized Python package.
- [Python environments and dependency resolution](references/dependencies.md) — Resolve runtime and dev dependencies.
- [Python static checks and evidence](references/quality-toolchain.md) — Interpret formatting, lint and typing checks.
- [Python packaging and distribution](references/release.md) — Publish package or CLI.

- [Python reproducible verification toolchain](references/deterministic-ci.md) — Implementing local and CI quality checks.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
