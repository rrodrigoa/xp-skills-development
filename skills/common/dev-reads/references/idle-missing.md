# Idle, missing, stale and low-volume signals

## When to load
A zero, gap or unstable ratio appears.

## Procedure
Separate observed zero (a fresh observation of no events), no matching series, stale sample, query failure, partial coverage and zero denominator. Check target inventory, scrape/export health, last sample time, labels, rollout changes and external demand. For low-volume SLI use longer windows, explicit minimum evidence, synthetic probes or counts with a documented policy. Avoid suppressing genuine outage when traffic disappears. A fill-zero transformation is valid only when the underlying observation is known healthy and zero is semantically correct. Mark unknown separately from healthy in dashboards and gates.

## Required evidence and acceptance
Replay fresh zero, no data, missing one region, zero denominator and stale values; verify distinct health and alert outcomes.

## Guardrails
A missing failure counter is not automatically evidence of no failures.
