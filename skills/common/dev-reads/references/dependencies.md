# READS at dependency and fan-out boundaries

## When to load
A service calls databases, APIs, tools or other services.

## Procedure
Record client-side attempt rate/error/duration separately from the overall logical operation. Distinguish dependency endpoint, operation class and timeout/circuit-open status with bounded dimensions. Availability includes dependency success as experienced by the caller, not just the remote service self-report. Track pool saturation, quotas and wait time; identify shared dependency blast radius. For parallel fan-out, measure overall critical path rather than adding durations. Map graceful degradation and fallback to actual user contract; a successful fallback may be healthy for availability but degraded for quality. Compare parent/child traces and client versus server perspectives to test hypotheses.

## Required evidence and acceptance
Simulate slow dependency, failed first attempt, fallback, fan-out partial failure and circuit-open; reconcile parent outcome with child attempts.

## Guardrails
Never multiply dependency availability as a prediction without an explicit independence model; correlation and shared failures matter.
