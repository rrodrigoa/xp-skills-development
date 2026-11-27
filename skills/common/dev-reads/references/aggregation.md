# Aggregation, populations and scope

## When to load
Combining signals across instances, regions or time.

## Procedure
Compare consistent dimensions and units; calculate rate per counter before summing so resets are handled. Sum good/bad counts across the intended population then divide, rather than average percentages with unequal traffic. For a region with 1 failure in 10 requests and another with 9 in 990, global error ratio is 10 in 1000, not the mean of regional percentages. Preserve per-region and critical-journey views to avoid hiding local impact. Aggregate histogram buckets only when compatible; percentile arithmetic is invalid. Treat replica deduplication, rollout overlap, late arrivals, scrape gaps and clock skew explicitly. Identify whether global views are weighted by events, time or business priority.

## Required evidence and acceptance
Reconcile aggregate with raw counts over the same interval; test skewed volumes, counter reset, mixed versions and missing series.

## Guardrails
Never silently average ratios, percentiles or incompatible time windows.
