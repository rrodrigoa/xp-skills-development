# Tempo, TraceQL and trace exploration

## When to load
Investigating distributed request or agent traces.

## Procedure
Use authorized service, operation, environment, time range, duration/outcome filters and trace IDs from logs or exemplars. Inspect span topology, dependency durations, error events, retry attempts and critical path; identify incomplete traces or sampling bias. Prefer bounded queries and narrow filters before scanning attributes. Use service graph/span-derived metrics for navigation only after checking sampling, aggregation and coverage. Trace-to-logs links preserve scope and time; verify trace ID correlation and tenant isolation. Compare multiple representative traces including successful control cases.

## Required evidence and acceptance
Known distributed request is discoverable and links to relevant logs and metrics; verify missing spans, sampled-out trace and async links are interpreted correctly.

## Guardrails
Do not assume an exemplar is representative or count sampled spans as exact request volume.
