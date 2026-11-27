# Formal property and correspondence evidence gate

## When to load
Approved policy requires a model or proof for a critical property.

## Implementation in the target project
Use dev-formal-verification formal-spec, proof-gates and model-correspondence. Inspect exact theorem/property, assumptions, bounds, proof axioms, negative controls, checker outcome and implementation linkage. Review property changes independently.

## Required evidence and acceptance
Bounded model check or accepted proof with exact scope and mapping; required timeout/unsupported run UNKNOWN; counterexample or unapproved weakening FAIL.

## Guardrails
Do not require formal verification universally or imply bounded models prove production code.
