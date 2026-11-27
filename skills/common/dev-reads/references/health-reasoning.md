# Health reasoning and cross-signal diagnosis

## When to load
Investigating a READS anomaly.

## Procedure
State exact service/operation, region, environment, time window, baseline, traffic population and data freshness. Start with user outcome and duration, check rate and availability independently, then use saturation/dependency telemetry to form competing explanations. Examples: rising queue wait with flat service time suggests constrained admission; falling R plus probe failure suggests ingress loss; increasing E with low D may be fast rejection; increasing D with steady E may precede exhaustion. Compare unaffected cohorts and deployment/config changes. Seek discriminating evidence in traces, logs and resource metrics; time correlation alone is not causation. Report blast radius, observed facts, hypotheses, counterevidence and next safe check.

## Required evidence and acceptance
Provide queries or evidence references with units, windows and sample counts, a ranked hypothesis list and explicit unknowns; verify recovery across all affected dimensions.

## Guardrails
Do not infer root cause from one panel or declare recovery solely because an alert resolved.
