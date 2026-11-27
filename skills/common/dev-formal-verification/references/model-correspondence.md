# Connect models and proofs to implementation

## When to load
Formal result is cited for a production change.

## Implementation in the target project
Map each modeled variable and transition to source owner, API and observed event; list abstracted effects and assumptions. Derive executable test sequences from model traces and counterexamples; compare code transitions against model and test serializer, persistence and numeric boundaries. Keep mapping versioned and rerun when relevant source/spec changes.

## Required evidence and acceptance
Traceability matrix with actual tests and code references; deviations explained and independently approved. Gate uses only claim within verified scope.

## Guardrails
Do not label entire system verified merely because a related algorithm or bounded model passes.
