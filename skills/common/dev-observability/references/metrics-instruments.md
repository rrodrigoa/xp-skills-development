# Metric instruments, temporality and lifecycle

## When to load
Selecting metric type or diagnosing metric math.

## Procedure
Use counters for monotonic event totals; up/down counters for additive changing occupancy where appropriate; gauges for observed current state; histograms for distributions. Define units consistently (e.g. seconds at the Prometheus boundary; verify OTel translation). Initialize known bounded series only if zero is meaningful; absence still requires coverage checks. Record histogram boundaries around decision thresholds and assess bucket cost. Cumulative versus delta temporality must match exporter/backend expectations; understand process resets and replica identity. Reuse instruments for process lifetime and avoid dynamic instrument creation. Measure actual exported samples, not only mock calls.

## Required evidence and acceptance
Known event totals and histogram count/sum/buckets survive collection; verify resets, concurrent updates, label limits, idle and exporter mapping.

## Guardrails
Do not use gauges for event counters, precomputed percentiles for fleet aggregation, or mix delta and cumulative values.
