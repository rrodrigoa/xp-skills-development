# Unit testing with pytest

## Use when
Testing policy, object invariants and pure functions.

## Avoid when
Testing private methods and incidental call counts.

## Implementation
Use arrange-act-assert, meaningful names, parameterized inputs, narrow fixtures and real collaborators when cheap; use explicit failure assertions.

## Verification and review
Tests fail for meaningful regressions, run independently and deterministically.
