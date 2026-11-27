# Inter-agent handoff contract

## When to load
Passing work between planning, implementation, verification and gate agents.

## Procedure
Send task ID, exact revision or working-tree identity, objective, constraints, risk, affected symbols, loaded skill paths and versions, decisions, acceptance tests, evidence references, unresolved gaps and next permitted action. Receiver confirms revision and scope before use.

## Required evidence and acceptance
Compact structured prose handoff, attributable artifacts and explicit unknowns; incompatible handoff rejected or refreshed.

## Guardrails
No raw secrets, hidden chain of thought or unsupported success assertions. A handoff is not authorization to expand scope.

## Operational evidence handoff
Record incident/operation, environment and tenant scope, query/window/time zone, backend freshness, deployed revision, counts/units, confidence, hypotheses and falsifying checks, approved action/rollback and recovery evidence. Reference data instead of transferring sensitive raw logs. A diagnostic handoff is not approval to mutate.
