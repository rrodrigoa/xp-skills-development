# Fixtures, fakes, mocks and stubs

## Use when
External or nondeterministic dependencies.

## Avoid when
Mocking implementation internals or using unrealistic fakes.

## Implementation
Inject port; fake stateful collaborator, stub canned results, mock interaction only when it is contract. Use autospec if mocking existing APIs; scope fixtures narrowly.

## Verification and review
Run contract tests against fake and real; avoid shared mutable fixtures.
