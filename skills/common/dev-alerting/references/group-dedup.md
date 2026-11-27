# Grouping, deduplication and inhibition

## When to load
Reducing alert storms without losing incident visibility.

## Procedure
Group related alert instances by stable service/environment/incident scope so notifications represent actionable work; use stable label identity and reasonable group wait/interval/repeat policy. Deduplicate equivalent alerts from multiple evaluators or migrate ownership explicitly. Inhibit dependent symptoms only when a verified higher-level incident explains them and operators retain affected-scope visibility. Avoid overly broad grouping that merges unrelated regions or tenants; preserve severity and route. Document which alert is authoritative and why; test incident fan-out and notification volume.

## Required evidence and acceptance
Simulate shared dependency outage and unrelated simultaneous fault; verify expected groups, suppression boundaries, route and resolved behavior.

## Guardrails
Do not silence all lower-level symptoms based solely on time overlap or group distinct incidents into one ambiguous page.
