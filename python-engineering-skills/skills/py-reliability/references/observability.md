# Metrics, logs and tracing

## Use when
Production services need diagnosis.

## Avoid when
High cardinality labels, sensitive payloads or alerts on every error.

## Implementation
Define outcome/latency/error metrics, trace boundaries with correlation IDs, redact content, use actionable SLO-based alerts; distinguish user vs dependency failures.

## Verification and review
Test instrumentation and redaction; document dashboards and alert ownership.
