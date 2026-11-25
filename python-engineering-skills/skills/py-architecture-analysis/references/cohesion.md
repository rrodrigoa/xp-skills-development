# Cohesion and responsibility analysis

## When to load
A module or class appears to contain unrelated behavior.

## Procedure
Map methods to fields, invariants, collaborators and reasons to change. Optionally use a documented LCOM variant: LCOM4 counts connected method groups joined by shared instance fields or internal calls. State treatment of constructors, properties and inherited members. Review semantic clusters and independent lifecycles.

## Required evidence and acceptance
Show member clusters, why responsibilities differ, mutation ownership and plausible extraction seams.

## Guardrails
Do not equate stateless utilities or framework callbacks with low-quality design. Never split solely to improve LCOM.
