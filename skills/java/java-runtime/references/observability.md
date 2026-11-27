# Java logging, metrics and tracing

## Shared guidance
dev-reliability: observability, operations

## When to load
Instrument service or worker.

## Language-specific decisions
Use approved SLF4J facade/backend and structured logging; avoid duplicate bindings. Propagate correlation through executor and async boundaries explicitly; use OpenTelemetry/Micrometer only where approved. Control cardinality and redact secrets. Expose readiness and resource saturation for services.

## Verification and evidence
Verify correlation across threads, error visibility, bounded labels and redaction; simulate dependency failure.

## Avoid
Logging full request bodies or assuming thread-local context automatically crosses async boundaries.

## Deep instrumentation
For provider/agent setup and signal ownership read local [OpenTelemetry instrumentation](otel-instrumentation.md); for async and logging use [telemetry context](telemetry-context.md). The canonical common skills are dev-reads and dev-observability; use dev-grafana and dev-alerting only for monitoring/alert tasks.
