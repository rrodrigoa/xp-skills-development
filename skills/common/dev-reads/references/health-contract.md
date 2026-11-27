# READS service health contract

## When to load
Defining health for a new or existing service.

## Procedure
Start with user journeys and critical operations, not available CPU charts. For each operation identify the consumer, service boundary, eligibility, start/end event, terminal outcomes, dependencies, expected traffic and capacity constraints. Specify each READS dimension with instrument, unit, scope, dimensions, aggregation, window, expected idle behavior, owner and dashboard/alert intent. Distinguish externally observed outcome from internal attempt and component health. Map every critical journey to a contract, including async completion or freshness where applicable. Record a justified non-applicability for a dimension rather than invent a proxy. Agree the definition with the service owner before changing metrics or SLOs.

## Required evidence and acceptance
Produce a revision-bound health contract and a coverage matrix from operation to measurement point to evidence; show positive, failure, idle and degraded cases.

## Guardrails
Do not equate service health with deployment readiness, host uptime or five arbitrary thresholds.
