---
name: py-reliability
description: "Engineer Python reliability, security, observability, concurrency, performance, data integrity and resilient I/O."
---
# Python Reliability

Identify trust boundaries, resource ownership, SLOs, failure modes and concurrency limits. Validate inputs, bound work and use explicit deadlines. Keep secrets and sensitive data out of logs. Prefer measured optimization. Test failures, cancellation, cleanup and recovery. Do not add retries without idempotency analysis.

## Reference selector
Read only relevant files from this list.

- [Security and trust boundaries](references/security-boundaries.md) — Processing user input, network, files or plugins.
- [Safe filesystem operations](references/filesystem.md) — Reading/writing user-controlled paths or archives.
- [Subprocess and terminal execution](references/subprocess.md) — CLI invokes other programs.
- [Async, threads and processes](references/async.md) — I/O concurrency or CPU parallelism.
- [Timeouts, retry and circuit breaker](references/resilience.md) — Remote operations have transient faults.
- [Metrics, logs and tracing](references/observability.md) — Production services need diagnosis.
- [Profiling and performance](references/performance.md) — Measured bottleneck or resource budget.
- [Caching and invalidation](references/caching.md) — Repeated expensive deterministic or versioned queries.
- [Transactions, idempotency and atomic writes](references/data-integrity.md) — Durable state and retried mutations.
- [Secrets and sensitive information](references/secrets.md) — Credentials, tokens or user data used.
- [Resource limits and backpressure](references/resource-bounds.md) — Potentially large input, queue or output.
- [Health, shutdown and recovery](references/operations.md) — Long-lived services or worker processes.
