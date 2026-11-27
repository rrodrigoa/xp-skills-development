# Instrumentation tests and end-to-end verification

## When to load
Testing changed telemetry or its consumers.

## Procedure
Use a deterministic clock and in-memory/recording test exporter where supported; assert semantic events, counts, dimensions and outcomes rather than internal implementation calls. Cover success, expected rejection, dependency failure, retry, timeout, cancellation, fallback, concurrency, resource cleanup and privacy. Test real collection/export translation in a representative environment: names, units, temporality, histogram boundaries and trace correlation. Reconcile known input and expected counts. Test dashboards and alert expressions against the same cases. Include overhead and fault injection for telemetry outages. Separate local, staging and production evidence; never claim live ingestion from unit tests.

## Required evidence and acceptance
Provide revision-bound test results and backend queries/samples for the deployed version, with timestamps and environment; list unavailable checks explicitly.

## Guardrails
No fabricated data, screenshot-only proof, or tests that assert merely that a logger was invoked.
