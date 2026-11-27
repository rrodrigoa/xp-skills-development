# Runtime, container and Kubernetes observability

## When to load
Operating deployed services and workers.

## Procedure
Correlate service health with workload/namespace/cluster identity, deployment revision, replicas, restarts, readiness and liveness, CPU throttling, memory pressure/OOM, disk, networking, pool and queue limits. Distinguish readiness (traffic eligibility), liveness (restart policy), startup and user availability. Use resource/USE signals as diagnosis and capacity evidence, not automatic proof of service health. For autoscaling observe desired/current replicas, scheduling lag, quota and rollout health. Use stable service-level metrics plus instance-level drilldown; avoid ephemeral identifiers as long-lived metric dimensions except where operationally justified.

## Required evidence and acceptance
Controlled rollout and failure show correct service outcomes, workload/resource attribution, restart handling and partial-replica impact.

## Guardrails
Do not make liveness depend on every remote dependency or page on each transient pod restart without actionability.
