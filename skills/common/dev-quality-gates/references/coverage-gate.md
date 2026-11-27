# Coverage regression and changed-code gate

## When to load
Coverage is configured as a quality measure.

## Procedure
Compare line and branch coverage with identical measurement scope, tool config, exclusions and revision. Evaluate changed executable lines separately; report numerator and denominator, uncovered paths and justified exclusions. Apply project-approved floors and regression tolerance.

## Required evidence and acceptance
Coverage artifacts for base/head and changed code, explicit denominator and high-risk uncovered decisions.

## Guardrails
No universal coverage percentage. Empty denominator is not applicable only if verified; 100 percent coverage does not establish correctness.
