---
name: py-testing
description: "Verify Python unit, integration, contract, concurrency, coverage and installed-artifact tests."
---
# Python Testing

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-testing and applicable dev-quality-gates. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [pytest and unittest organization](references/pytest.md) — Implement Python tests.
- [Python async testing](references/async-tests.md) — Test coroutine and cancellation behavior.
- [Hypothesis and Python coverage](references/property-coverage.md) — Exercise invariants and test effectiveness.
- [Python installed artifact and integration tests](references/installed-tests.md) — Verify a library or CLI release.
- [Python observability testing and verification](references/telemetry-tests.md) — Testing instrumentation changes before merge or release.

- [Python deterministic tests and reproducible failures](references/deterministic-tests.md) — Testing nondeterministic behavior and rule enforcement.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
