# Java async telemetry context and structured logging

## Shared guidance
dev-observability: context-propagation, structured-logs, traces-spans, failure-isolation; dev-reads: async-streaming

## When to load
Instrumenting concurrent workflows, executors or message boundaries.

## Procedure
Use OTel Context/Scope and supported executor instrumentation; MDC is thread-local unless explicitly propagated, and pooled/virtual threads do not justify assuming context inheritance. Wrap tasks only once, restore scope and MDC in finally and avoid cross-tenant contamination. For CompletableFuture, reactive pipelines and message consumers verify framework-specific context propagation and cancellation. Measure executor queue wait, pool occupancy, rejected tasks and actual completion separately. Use SLF4J structured logging and one approved backend; avoid duplicate bridges and synchronous remote logging in hot paths.

## Required evidence and acceptance
Concurrent runs with distinct contexts, timeout, cancellation and pooled task reuse show correct trace/log correlation, resource cleanup, no leaks and bounded overhead.

## Guardrails
Never use trace context as authorization or log unredacted request/agent payloads.
