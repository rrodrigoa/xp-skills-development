# SLI, SLO, SLA and error budgets

## When to load
Defining measurable reliability targets.

## Procedure
Define SLI as the measurement, SLO as an approved target over a stated window, SLA as an external commitment with separate consequences. For event-based SLI specify eligible events and good events; compute the good fraction from sums of compatible counters over the same window. For target 99.9%, allowed bad fraction is 0.1%; 1,000,000 eligible events permit 1,000 bad events over the objective window. Burn rate equals observed bad fraction divided by allowed bad fraction; a burn of 10 means ten times sustainable consumption, not ten percent budget spent. Track remaining error budget with actual window totals; for varying traffic the time-window burn approximation is not exact budget consumption. Define exclusions, late data, unknown coverage and low traffic before adoption.

## Required evidence and acceptance
Owner-approved SLI definition, target/window, replay with known outcomes and documented budget math; verify policy on missing data and denominator zero.

## Guardrails
Do not create an SLO for every metric, infer an SLA from an internal target, or invent universal reliability targets.
