# Versioned telemetry schema and semantic contracts

## When to load
Adding, changing or removing telemetry.

## Procedure
Record stable name, semantic meaning, signal kind, type/unit/temporality, start/end points, population, permitted attributes and cardinality bounds, error taxonomy, owner, consumers, sensitivity and version. Prefer applicable pinned OpenTelemetry semantic conventions; use a documented project namespace for gaps. Distinguish OTel names/units from backend translation (Prometheus suffixes and resource labels may differ). Do not assume vendor exports retain exact names. Track dashboard, SLO, alert and downstream consumers; use parallel migration with explicit cutover, avoid double counting old and new series, and remove legacy only after verified consumer migration.

## Required evidence and acceptance
Contract diff, emitted and backend-observed names/types/units, label enumeration, query compatibility and migration/rollback evidence.

## Guardrails
Do not repurpose a metric name when its population, units or meaning changes.
