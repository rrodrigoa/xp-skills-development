# Architecture contract authoring

## When to load
Defining enforceable dependency and ownership rules.

## Procedure
For each rule assign stable ID, scope and units, rationale, allowed and prohibited edge direction, edge types, exceptions, baseline, evidence method, severity, owner and effective policy version. Specify whether transitive dependencies count. Define fixtures for allowed, forbidden and unresolved cases. Examples: domain cannot import concrete I/O; presentation cannot implement authorization policy; composition root may wire adapters.

## Required evidence and acceptance
A reviewer can decide applicability and pass/fail from the rule alone. Record concrete positive and negative examples and enforcement limits.

## Guardrails
Do not enforce invented folder layouts; bind to actual packages. Unknown evidence is not pass. Any deviation needs approved scope and expiry.
