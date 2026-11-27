# READS alert selection by dimension

## When to load
Translating the service health contract into candidate alerts.

## Procedure
R: alert on unexpected traffic loss only when expected demand, upstream signal or synthetic probe corroborates it; use arrival/completion imbalance with backlog risk for workers. E: alert on sustained terminal error ratio or burn with count/coverage, not individual retry errors; dependency failure is often diagnosis or an owned imminent risk. A: page on approved user-journey SLO burn or external probe failure with appropriate location quorum and coverage. D: use deadline-good fraction burn or a sustained latency distribution with count, separate fast failures and queue age. S: page for imminent resource exhaustion when there is a timely prevention action; use capacity planning tickets for slow trends. Link multiple dimensions to the same incident where appropriate; avoid five pages per outage. Document no-traffic handling, severity, route, and runbook per candidate.

## Required evidence and acceptance
For each dimension document candidate or reason for dashboard-only/non-applicable; replay an ingress outage, retry storm, queue backlog and resource exhaustion; show expected consolidated notifications.

## Guardrails
READS does not require a paging alert for every dimension. Do not confuse a dimension with a root cause.
