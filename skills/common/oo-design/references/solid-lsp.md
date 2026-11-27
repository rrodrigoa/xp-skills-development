# Liskov substitution

## Use when
Several implementations claim one interface.

## Avoid when
Unrelated objects that merely share a method name.

## Implementation
Specify preconditions, postconditions, errors and side effects. Subtypes must preserve observable promises; prefer composition if they cannot.

## Verification and review
Run the same contract tests against every implementation.
