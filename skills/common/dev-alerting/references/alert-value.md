# Alert quality, value and continuous improvement

## When to load
Reviewing alert portfolio and fatigue.

## Procedure
Track alert instances, notifications, grouped incidents, actionable responses, false positives, duplicates, missed incidents, time-to-detect/ack/mitigate, flapping, stale ownership and no-data/query errors. Define each denominator and dedup unit; a notification count is not incident count. Classify outcome with responder evidence; sample missed incidents from postmortems rather than only fired alerts. Review per service/severity and workload, compare changes before/after with traffic and incident mix. If adopting an Alert Value Index, document local formula, weights, calibration, missing labels and intended decisions; no universal score. Remove or downgrade alerts only after proving replacement coverage and getting approval.

## Required evidence and acceptance
Portfolio report with counts/denominators, representative false-positive and missed-incident evidence, proposed remediation, owner and follow-up.

## Guardrails
Do not optimize for fewer pages alone, punish valid alerts with no immediate mitigation, or use an uncalibrated composite score as a mandatory gate.
