# Interfaces and abstract base types

## Use when
Multiple implementations or external boundaries need a contract.

## Avoid when
A concrete internal type has no meaningful substitution.

## Implementation
Choose structural or nominal interfaces where the language supports them; use an abstract base type only when shared lifecycle or a stable template is necessary. Verify substitutability by behavior rather than interface shape alone.

## Verification and review
Static check plus behavioral contract tests.
