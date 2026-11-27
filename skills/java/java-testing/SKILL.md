---
name: java-testing
description: "Verify Java unit, integration, contract, concurrency, coverage and installed-artifact tests."
---
# Java Testing

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-testing and applicable dev-quality-gates. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [JUnit platform and test organization](references/junit.md) — Add Java unit and behavioral tests.
- [Java fakes and Mockito](references/doubles.md) — Isolate external dependencies.
- [Java integration and Testcontainers](references/integration.md) — Test database, broker, HTTP or deployment behavior.
- [Java concurrency and async tests](references/concurrency.md) — Test executors, futures or concurrent state.
- [JaCoCo and mutation testing](references/coverage-mutation.md) — Assess Java test quality.
- [Java installed artifact and compatibility tests](references/artifact-tests.md) — Verify JAR/library/CLI.
- [Java observability testing and verification](references/telemetry-tests.md) — Testing instrumentation changes before merge or release.

- [Java deterministic tests and reproducible failures](references/deterministic-tests.md) — Testing nondeterministic behavior and rule enforcement.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
