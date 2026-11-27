# Alert testing, shadow evaluation and rollout

## When to load
Introducing or modifying alert rules or routing.

## Procedure
Build a case table for healthy, threshold boundary, transient spike, sustained breach, recovery, missing data, zero volume, partial cohort, duplicate and dependency outage. Verify evaluation times/labels, pending and recovery, page/ticket severity, grouping, route and notification delivery separately. Backtest historical incidents and normal periods; shadow or route to authorized nonpaging test receiver during calibration, with explicit duration and monitoring. Compare old/new rule coverage and duplicate notifications before cutover; maintain rollback and review after activation. Avoid simulating disruptive production incidents without approval.

## Required evidence and acceptance
Revision-bound expected/actual state timeline, query/rule results, test receiver proof, backtest and rollback plan. Record untested live delivery as UNKNOWN if required.

## Guardrails
Do not fire real pages to test without coordination, or disable existing coverage before verifying replacement.
