# Testing strategy and risk

## Use when
New feature or project test plan.

## Avoid when
All tests at E2E level or all mocked unit tests.

## Implementation
Map risks to unit, component, contract, integration and E2E levels. Cover positives, negatives, boundary and abuse paths; select lowest sufficient level.

## Verification and review
Each critical requirement has observable assertions; track untested external risks.

For deterministic adoption, use dev-deterministic requirements-oracles, dev-enforcement check-fixtures and dev-runtime-verification independent-oracles. Establish negative controls and record actual discovered tests, candidate revision and environment. Use dev-formal-verification method-selection only when a high-risk property warrants it.
