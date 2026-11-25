# Branch by abstraction

## When to load
Replacing a dependency or implementation while keeping releases viable.

## Procedure
Introduce a narrow seam around old implementation; route callers through it without behavior change. Add new implementation and shared contract tests; migrate one cohort at a time with explicit selection, then remove old path when exit criteria are met.

## Required evidence and acceptance
Caller migration inventory, equivalent contract tests, switch/rollback procedure and removal criteria.

## Guardrails
Avoid indefinite dual paths. Never duplicate irreversible side effects when comparing implementations.
