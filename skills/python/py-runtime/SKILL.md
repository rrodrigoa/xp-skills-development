---
name: py-runtime
description: "Handle Python concurrency, resource ownership, process safety, performance and runtime reliability."
---
# Python Runtime

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-reliability and relevant dev-implementation cards. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Python threads, processes and asyncio](references/concurrency.md) — Choose concurrency or parallelism.
- [Python context managers and cleanup](references/resource-lifecycle.md) — Manage files, sessions, locks and owned clients.
- [Python subprocess and filesystem safety](references/processes.md) — Launch tools or access files.
- [Python performance and diagnostics](references/profiling.md) — Investigate CPU, memory or I/O regressions.
- [Python OpenTelemetry and metric ownership](references/otel-instrumentation.md) — Adding or changing telemetry in a service or library.
- [Python async telemetry context and structured logging](references/telemetry-context.md) — Instrumenting concurrent workflows, executors or message boundaries.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
