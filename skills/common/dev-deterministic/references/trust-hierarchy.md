# Trust hierarchy and constraint selection

## When to load
A new standard, recurring defect or adoption plan.

## Implementation in the target project
For each failure identify the violated invariant, causal mechanism, affected surface and canonical good example. Prefer removing the invalid operation from the public API or type model; next introduce a structural check, then an executable behavioral oracle; add runtime/formal verification for remaining risk. Keep prose for intent and exceptions. Record why a cheaper layer cannot suffice. Measure enforcement and migration costs rather than rule count.

## Required evidence and acceptance
Demonstrate an invalid candidate rejected or impossible through supported interfaces, a valid candidate accepted, and a repeatable invocation. Report remaining bypass paths and approval requirements.

## Guardrails
A deterministic checker may encode the wrong requirement. Do not equate repeatability with truth or force every judgment into lint.
