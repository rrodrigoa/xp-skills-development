# Local checks and protected CI enforcement

## When to load
Moving a useful check into a required gate.

## Implementation in the target project
Inventory existing entry points and CI contexts; choose one canonical command per check, pinned environment and expected exit behavior. Run locally and in CI; verify test discovery, timeouts, skipped jobs, path filters, caching and artifact identity. Require exact context for candidate/merge revision through authorized branch policy. Separate fast developer feedback from full verification.

## Required evidence and acceptance
Capture actual local/CI results and branch-rule evidence if required; failing fixture prevents green status; missing job is not pass.

## Guardrails
Do not change branch protection, permissions or workflows without authority. A local check does not prove remote enforcement.
