# Actionable annotations, runbooks and response instructions

## When to load
Preparing an alert for on-call use.

## Procedure
Include concise impact, affected service/operation/region, condition and time window, evidence links preserving scope, severity/owner and runbook. Runbook begins with verification of data freshness and user impact; list safe read-only checks, relevant READS and dependency views, decision points, escalation and known reversible mitigations with prerequisites and authorization. State when not to act, risks, rollback and recovery evidence. Avoid stale links or environment-specific destructive commands. Keep operational guidance versioned with service changes and validate accessibility for on-call roles.

## Required evidence and acceptance
An unfamiliar responder can follow a dry-run scenario, find correct dashboards and know escalation/authorization boundaries; verify links and scope.

## Guardrails
Do not put secrets, raw user payloads or unreviewed destructive actions in notification annotations.
