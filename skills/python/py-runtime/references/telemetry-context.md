# Python async telemetry context and structured logging

## Shared guidance
dev-observability: context-propagation, structured-logs, traces-spans, failure-isolation; dev-reads: async-streaming

## When to load
Instrumenting concurrent workflows, executors or message boundaries.

## Procedure
Use contextvars and the approved OTel context APIs to scope trace/log context in asyncio; check thread executor and process boundary propagation explicitly rather than assuming inheritance. Use structured logging integration that enriches current context without attaching handlers repeatedly. Close/restore scope on cancellation, timeouts and exceptions. Track queue age, in-flight work and worker occupancy from owners; distinguish async event loop lag from CPU saturation. Avoid blocking exporter/network calls on event loop and bound shutdown flush. For CLI keep stdout machine contract and send permitted diagnostics to stderr.

## Required evidence and acceptance
Concurrent runs with distinct contexts, timeout, cancellation and pooled task reuse show correct trace/log correlation, resource cleanup, no leaks and bounded overhead.

## Guardrails
Never use trace context as authorization or log unredacted request/agent payloads.
