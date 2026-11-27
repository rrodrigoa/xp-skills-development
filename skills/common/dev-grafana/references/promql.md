# Prometheus and PromQL query reasoning

## When to load
Writing or reviewing metric queries.

## Procedure
Inspect actual metric type, units, series labels, scrape interval and temporal coverage first. For counters derive rate or increase per series before aggregation; select a range sufficiently larger than sample interval, then sum by stable scope. Compute failure ratio with matching numerator/denominator labels and time windows; handle denominator zero and missing series explicitly. Use gauge aggregates that match question (sum occupancy, max hotspot, min headroom). For histograms aggregate compatible bucket rates with required bucket boundary dimension for classic histograms, then derive quantile; native histograms use supported semantics. Check vector matching and avoid accidental many-to-many joins; compare raw samples and expected count. For alert rules verify concrete windows in backend context, not dashboard macros by assumption.

## Required evidence and acceptance
Use known counts, reset, missing series, unequal regional traffic and histogram distributions; validate expression against actual backend/version, query range and cardinality.

## Guardrails
Do not average p95, take rate of gauge, sum counters before rate or infer zero from absent without independent coverage.
