# SLO burn-rate alerts and multiwindow design

## When to load
Alerting on reliability objective consumption.

## Procedure
Burn rate is bad-event fraction divided by allowed bad fraction. Select thresholds and paired long/short windows to match approved budget-spend and detection objectives. For a 30-day SLO, illustrative Google SRE pairs are 14.4 over one hour and five minutes, and 6 over six hours and thirty minutes, both windows exceeding their respective same threshold for each pair; 14.4 times one hour divided by 720 hours is approximately 2% of budget under uniform traffic. A slower pair can drive a ticket instead of a page. Derive for actual window and traffic assumptions; evaluate eligible count, low-volume behavior, probe outages, exclusion policy and freshness. Keep separate SLOs for materially different journeys; do not average burn across incompatible populations.

## Required evidence and acceptance
Replay fast outage, sustained slow burn, brief spike, recovery, sparse traffic and missing data; verify both windows, expected page/ticket timing and budget math.

## Guardrails
Example values are not mandated thresholds; do not use OR between paired windows when the intended policy requires AND.
