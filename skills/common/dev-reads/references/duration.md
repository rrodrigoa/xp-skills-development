# D — Duration and latency distribution

## When to load
Measuring responsiveness and long-tail delays.

## Procedure
Use monotonic elapsed time around the user-visible operation, with explicit treatment of queueing, retries, streaming first result and final completion. Separate client, server, dependency and queue wait times; avoid summing parallel span durations. Record distributions (histograms with useful boundaries including the SLO threshold) and counts, not only means. Derive percentiles after aggregating compatible histograms; report sample size, window and population. Compare success and failure latency so fast failures cannot hide impact. For async measure age from acceptance to durable outcome; track censored in-flight work separately. For an SLI prefer the fraction completed within an approved threshold over inferring it from p95.

## Required evidence and acceptance
Inject delays before execution, during retry and after first streamed token; verify end-to-end duration, bucket boundaries, cancellation and low-volume behavior.

## Guardrails
Never average instance p95s or use wall-clock subtraction for local elapsed time when clocks can change.
