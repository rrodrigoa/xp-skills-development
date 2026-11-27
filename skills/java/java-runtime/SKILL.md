---
name: java-runtime
description: "Handle Java concurrency, resource ownership, process safety, performance and runtime reliability."
---
# Java Runtime

This is a language overlay, not a separate engineering standard. Select the corresponding common skill first: dev-reliability and relevant dev-implementation cards. Read only the matching shared card and language card. Shared card names below resolve through installed skill discovery or the source checkout under `skills/common/`; do not search recursively or load entire catalogs. Respect the actual project runtime version, dependency policy, approved tools and architecture contracts.

## Reference selector

- [Java threads, executors and virtual threads](references/concurrency.md) — Choose blocking or asynchronous execution.
- [Java memory model and shared state](references/memory-model.md) — Concurrently access mutable objects or caches.
- [Java AutoCloseable and lifecycle](references/resources.md) — Own streams, sockets, JDBC connections or executors.
- [Java ProcessBuilder and filesystem safety](references/processes.md) — Run subprocess or read/write paths.
- [JVM performance, JFR and JMH](references/profiling.md) — Investigate Java CPU, allocation or latency regression.
- [Java logging, metrics and tracing](references/observability.md) — Instrument service or worker.
- [Java framework and transaction boundaries](references/spring-boundaries.md) — Work in existing Spring or Jakarta application.
- [Java OpenTelemetry and metric ownership](references/otel-instrumentation.md) — Adding or changing telemetry in a service or library.
- [Java async telemetry context and structured logging](references/telemetry-context.md) — Instrumenting concurrent workflows, executors or message boundaries.

Report actual verification and any unsupported feature, missing evidence or version constraint. Language idioms do not weaken shared behavioral, security or gate requirements.
