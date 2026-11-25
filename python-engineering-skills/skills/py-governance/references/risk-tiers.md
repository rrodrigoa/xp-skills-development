# Risk classification and proportional controls

## When to load
Choosing review depth and required evidence.

## Procedure
Use project-approved tiers. Suggested low: docs or isolated nonbehavioral changes; normal: feature/bug with bounded impact; high: public contract, persistence, security, production operations, agent permissions or irreversible effects. Evaluate actual dependencies and blast radius; increase requirements for uncertain high-impact areas.

## Required evidence and acceptance
Risk tier rationale, impacted contracts, required checks and approvals; unknown risk escalated rather than silently downgraded.

## Guardrails
No size-only classification. A one-line auth change can be high risk; don't force unrelated architecture ceremony for typo fixes.
