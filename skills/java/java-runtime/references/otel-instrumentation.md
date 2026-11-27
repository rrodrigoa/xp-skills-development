# Java OpenTelemetry and metric ownership

## Shared guidance
dev-observability: instrumentation-plan, metrics-instruments, auto-manual, otel-pipeline; dev-reads: health-contract

## When to load
Adding or changing telemetry in a service or library.

## Procedure
Inspect existing Java agent, framework Micrometer registry and OpenTelemetry SDK/bridge before adding instruments. Libraries use the host-approved API, not a second global SDK. Reuse meter/tracer or registry handles; define whether timers and histograms publish buckets or client-side percentiles, and verify unit/label translation to backend. Use monotonic elapsed time, try-with-resources or explicit finally for scopes, and preserve the original exception. Avoid counting both AOP and manually timed operations unless they represent distinct boundaries. For Spring, distinguish HTTP observations from business result, async or transaction completion. Align JVM/JDK/agent/instrumentation versions and verify exporter lifecycle/shutdown.

## Required evidence and acceptance
Known workload produces exact domain counts, compatible histogram and trace hierarchy in test and representative backend; verify retry/cancel, duplicate instrumentation, exporter outage and overhead.

## Guardrails
Do not add another provider, emit high-cardinality request IDs in metrics or assume agent instrumentation captures domain outcomes.
