# S — Saturation and capacity headroom

## When to load
Measuring approaching limits before widespread failure.

## Procedure
Identify the actual constrained resource per subsystem: worker slots, bounded queue, connection pool, CPU run queue, memory pressure, disk or network I/O, GPU memory, quotas or external capacity. Record capacity and occupied/queued work, wait duration, rejections and time near limit. Derive headroom only if denominator is meaningful and comparable. Distinguish utilization (busy fraction) from saturation (unserved demand or delay); high utilization can be healthy and low CPU can coexist with blocked pools. Assess bottlenecks per shard/region and hottest instances, not only fleet means. Consider change in arrival versus service rate, time to fill, backpressure and autoscaling lag.

## Required evidence and acceptance
Controlled load approaches and exceeds a known limit; show queue wait, headroom, rejection, user latency, recovery and stable behavior when capacity is unknown.

## Guardrails
Do not substitute CPU percentage for every resource or treat unbounded queues as unlimited capacity.
