# Baseline and ratchet enforceable debt

## When to load
Existing code fails a new rule.

## Implementation in the target project
Inventory violations with stable fingerprint, scope, source revision and ownership. Choose approved no-new/no-worsened policy, accounting for renamed files and moved symbols. Preserve baseline under independent change control; migrate representative issues and remove resolved entries only after verification. Run checker on base and candidate using equivalent scope.

## Required evidence and acceptance
New violations fail and resolved debt cannot reappear unnoticed; baseline changes are reviewed separately.

## Guardrails
Do not silently regenerate baseline or hide old violations in global exclusions. Track rule-version migration explicitly.
