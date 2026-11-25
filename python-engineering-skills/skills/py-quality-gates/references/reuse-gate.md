# Reuse, duplication and object design gate

## When to load
New functions, classes, services or repeated policies are introduced.

## Procedure
Search existing implementations and consumers. Review ownership, invariants, lifetime and semantic duplication; identify whether abstraction is meaningful. Require a concrete conflicting rule or demonstrated risk for blocking, otherwise recommend improvement. Inspect for empty wrappers, static-only classes and feature envy.

## Required evidence and acceptance
Locations of existing/new behavior, justification for reuse or separation and observed risk; confirmed violations mapped to policy.

## Guardrails
No function/class quota. Similar syntax or a justified pure function is not a violation.
