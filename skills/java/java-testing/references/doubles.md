# Java fakes and Mockito

## Shared guidance
dev-testing: fixtures-doubles, contract

## When to load
Isolate external dependencies.

## Language-specific decisions
Inject interfaces/clock/executor and favor simple fakes when contract is meaningful. Use Mockito when interaction verification is required; strict stubbing where configured. Avoid mocking value objects or private methods. Use same contract suite against real adapters.

## Verification and evidence
Test negative interactions only when contract requires them; verify real implementation separately and no stale stubs.

## Avoid
Deep stubs, blanket mocks, verifying every internal method call.
