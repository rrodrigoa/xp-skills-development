# R — Request rate and workload accounting

## When to load
Measuring demand, throughput and dropped work.

## Procedure
Count eligible logical operations at the ingress or acceptance boundary; distinguish offered, admitted, started and completed work. Expose monotonically increasing counters for each required event and derive rate over time; do not emit precomputed per-second gauges as the only source. Separate attempts, retries, fan-out, duplicates, throttled and rejected requests from logical demand. For batches count batches and items with distinct units; for streams record events, bytes and processing progress separately. Aggregate counts before ratios. Segment by bounded operation and region, not raw path or request ID. Interpret a falling rate with external demand and synthetic checks: a broken ingress may appear idle.

## Required evidence and acceptance
For a known workload of 100 logical calls with 20 retries verify 100 demand events and 120 attempt events; validate restart/reset, burst, idle and rejected-request behavior.

## Guardrails
Completion rate can lag arrival rate; do not use the two interchangeably or infer availability from traffic alone.
