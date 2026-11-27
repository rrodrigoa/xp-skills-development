# Enforceable engineering constraints gate

## When to load
Architecture/API/check changes or repeated defect remediation.

## Implementation in the target project
Use dev-deterministic trust-hierarchy and dev-enforcement rule-contract/check-fixtures. Inspect approved invariant, API constraint/check scope, good/bad fixtures, legitimate exceptions and baseline. Confirm check executes locally and at required CI context. If constraint is not machine-enforceable, require documented residual judgment under approved policy.

## Required evidence and acceptance
Revision-bound evidence of valid and invalid cases, check identity and scope; required missing check UNKNOWN, known prohibited bypass FAIL.

## Guardrails
Do not require custom lint for every judgment; GOV-02 covers manipulation.
