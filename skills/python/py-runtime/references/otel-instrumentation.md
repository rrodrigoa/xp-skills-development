# Python OpenTelemetry and metric ownership

## Shared guidance
dev-observability: instrumentation-plan, metrics-instruments, auto-manual, otel-pipeline; dev-reads: health-contract

## When to load
Adding or changing telemetry in a service or library.

## Procedure
Use existing OTel API and SDK/provider configuration; a library uses the API without installing a global SDK or exporter. Inspect auto-instrumentation for framework/client/database edges and add manual domain instruments only for gaps. Reuse meter/tracer handles and use appropriate counters, histograms and callbacks. Define seconds/unit mapping from OTel to backend and check histogram boundaries and temporality. Use monotonic timing and try/finally or context managers to close spans and terminal observations; preserve cancellation and original exception. For multiprocess workers verify aggregation and distinct resource identity, and initialize exporter lifecycle safely per process. Check prometheus_client multiprocess behavior if already used rather than assume normal registry semantics.

## Required evidence and acceptance
Known workload produces exact domain counts, compatible histogram and trace hierarchy in test and representative backend; verify retry/cancel, duplicate instrumentation, exporter outage and overhead.

## Guardrails
Do not add another provider, emit high-cardinality request IDs in metrics or assume agent instrumentation captures domain outcomes.
