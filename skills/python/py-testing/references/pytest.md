# pytest and unittest organization

## Shared guidance
dev-testing: unit-tests, fixtures-doubles, test-strategy

## When to load
Implement Python tests.

## Language-specific decisions
Follow existing pytest or unittest conventions; parameterize cases, scope fixtures narrowly, prefer behavior-level assertions and deterministic fakes. Patch where a dependency is looked up only if injection is impractical.

## Verification and evidence
Verify collected test counts, positive/negative assertions, teardown and repeatability.

## Avoid
Mocking private implementation details or broad autouse fixtures hiding state.
