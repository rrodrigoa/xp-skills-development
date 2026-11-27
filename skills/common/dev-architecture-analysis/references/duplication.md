# Duplication and semantic reuse

## When to load
Investigating copy-paste and repeated domain policies.

## Procedure
Distinguish token/structural duplication from semantic duplication. Compare callers, invariants, side effects and expected future changes; identify the canonical owner and differences that must remain. Use normalized clone detection only as a lead and exclude generated code where policy permits.

## Required evidence and acceptance
Provide both locations, duplicated behavior, differences, reuse proposal and characterization cases.

## Guardrails
Similar syntax can implement distinct policies; do not unify unrelated concerns just to reduce duplication percentage.
