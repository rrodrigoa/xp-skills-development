# Counterexample-driven debugging

## When to load
Model checker, prover or property test finds violation.

## Implementation in the target project
Retain original failing trace and environment; minimize while preserving violated property. Translate abstract steps into concrete inputs, timing and fault injections. Determine whether spec, assumptions or implementation are wrong; seek approval for intent changes. Fix root cause and rerun checker plus regression, including valid trace.

## Required evidence and acceptance
Reproducible failure on defective model/code and pass after fix, with unchanged approved property or reviewed spec change.

## Guardrails
Do not remove state transitions or weaken property just to make model pass.
