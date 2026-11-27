# Distributed traces and meaningful spans

## When to load
Instrumenting multi-step operations or dependencies.

## Procedure
Model spans as bounded operations with stable low-cardinality names and correct parent/child/link relationships. Use server/client/producer/consumer/internal kinds as appropriate; record start/end, outcome and bounded attributes. Mark span error according to applicable conventions and user contract; record exceptions selectively and safely. Use span events for significant points, not arbitrary logs. For queue fan-in/fan-out or long-lived workflows use links when parent-child would misrepresent causality. Close spans on success, failure, timeout and cancellation. Correlate logs and exemplars through trace IDs; understand sampling means traces are not exhaustive.

## Required evidence and acceptance
Inspect trace topology for success, failure, retries, parallel calls and async work; verify span lifecycle, errors, cross-service propagation and sampled/unsampled behavior.

## Guardrails
Do not name spans with full URLs, IDs or prompt text; do not infer total traffic from sampled traces without a valid estimator.
