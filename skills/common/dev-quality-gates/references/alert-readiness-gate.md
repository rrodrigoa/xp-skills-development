# Alert actionability, routing and response readiness gate

## When to load
Alert rules, SLOs, notification policies, runbooks or critical behavior change.

## Procedure
Use dev-alerting alert-contract, testing-rollout and missing-data. Verify impact, eligibility, condition/window/state, severity, labels, ownership, route, grouping, maintenance scope, runbook and recovery. Test actual evaluation and authorized notification delivery separately; check old/new coverage, shadow/backtest results and source-of-truth control. Verify automated actions remain explicitly authorized and bounded.

## Required evidence and acceptance
Approved rule contract, state/notification evidence, test receiver proof when required, coverage diff, rollback and independent approval.

## Guardrails
No unauthorized silencing/threshold changes, no claims of delivered page based on rule firing; missing required evidence is UNKNOWN.
