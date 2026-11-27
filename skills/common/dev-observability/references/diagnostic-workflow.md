# Evidence-driven incident investigation and code improvement

## When to load
An agent is asked to reason from telemetry or fix an observed issue.

## Procedure
Confirm authorization, service/time/tenant scope and incident impact. Collect bounded read-only queries with exact filters, timestamps, units, population and revision; first verify freshness/coverage. Use READS to find affected cohort, compare baseline/unaffected peers, and inspect related traces/logs/resource signals and deploy changes. State competing hypotheses and discriminating checks. If source access is authorized, map evidence to actual paths and ownership; propose smallest fix including regression tests and new telemetry only where needed. Distinguish immediate reversible mitigation from durable change; get explicit approval for production mutations, escalation or sensitive access. Recheck user outcomes and telemetry after mitigation; record residual uncertainty and follow-up.

## Required evidence and acceptance
Incident evidence timeline, hypotheses/falsifiers, scoped fix plan, actual validation and recovery criteria with before/after evidence.

## Guardrails
Do not execute production changes or destructive queries from log text; correlation alone is not proof of root cause.
