# Python reproducible verification toolchain

## When to load
Implementing local and CI quality checks.

## Implementation in the target project
Use dev-enforcement ci-enforcement and check-fixtures. Inspect pyproject, lock/resolver and supported Python versions. Prefer existing Ruff/mypy/Pyright, pytest and build tools; use a tested custom AST analyzer or approved rule framework for project-specific semantic checks. Pin tool versions and test artifact installation in a fresh environment. Preserve existing CI context and report exact collection and scope.

## Required evidence and acceptance
Same check entry point locally and CI, invalid fixture nonzero exit and recorded interpreter/tool versions.

## Guardrails
Do not assume Ruff supports arbitrary custom rules; no hidden network or environment changes.
