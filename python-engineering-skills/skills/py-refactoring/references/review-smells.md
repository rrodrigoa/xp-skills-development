# Code smells and architecture review

## Use when
Reviewing AI-produced or sprawling code.

## Avoid when
Automatic rejection based on class count or arbitrary LOC.

## Implementation
Look for shared mutable globals, primitive obsession, feature envy, shotgun surgery, boolean flags, dead code, static-only classes, vague names, repeated branching and test-only implementation leaks. Rank by impact, propose smallest repair.

## Verification and review
Give path and line evidence, consequence, recommendation and tests; metrics are signals not proof.
