# Sampling, exemplars and representativeness

## When to load
Controlling trace volume or investigating rare events.

## Procedure
Choose head sampling for early predictable cost, tail sampling for completed-trace policy where the infrastructure supports complete trace routing, or a deliberate combination with documented limitations. Preserve error/slow traces within approved cost and privacy budgets; understand tail sampling memory and late spans. Do not derive exact READS counters from biased sampled traces; use independent metrics or a validated estimator with sampling weights. Use exemplars as optional links from metric observations to retained traces, not a requirement that every observation has a trace. Audit dropped and incomplete traces and coverage by operation/outcome.

## Required evidence and acceptance
Controlled traffic with known rare errors and slow cases demonstrates sampling behavior, cost, trace completeness and independent metric accuracy.

## Guardrails
Do not promise all errors are retained when upstream head sampling or queue drops already discard them.
