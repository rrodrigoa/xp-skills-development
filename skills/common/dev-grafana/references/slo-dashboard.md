# SLO and error-budget dashboards

## When to load
Visualizing reliability objectives and remaining budget.

## Procedure
Present target, window, measured SLI, eligible event count or intervals, bad events, remaining budget and data coverage. Show short/long burn rates, trend, affected critical journey and active alerts; define ratio units and exclusions. Use event-weighted window totals for exact event budget, not average of short-window percentages. Show historical change when target or eligible population changes rather than merging incompatible definitions. Separate synthetic and passive measurement where they represent different populations; mark unknown. If using Grafana SLO tooling, verify edition/plugin availability and generated rule/route ownership.

## Required evidence and acceptance
Replay a known failure population and no-traffic window; reconcile dashboard budget to independent calculation and alert thresholds.

## Guardrails
Do not display 100% success for undefined SLI or silently compare differently defined historical objectives.
