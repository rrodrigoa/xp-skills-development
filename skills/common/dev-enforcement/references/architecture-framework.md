# Framework and paved-path APIs

## When to load
Recurring decisions are hard for feature agents.

## Implementation in the target project
Identify high-frequency choices and provide a narrow supported abstraction with predictable lifecycle, defaults and extension points. Place low-level capability in controlled infrastructure; enforce caller boundaries separately. Document how to reach the API with one canonical example and useful error diagnostics. Migrate one feature and measure ease and overhead.

## Required evidence and acceptance
Valid feature can be implemented via paved path; prohibited bypass fails; underlying framework has its own tests and controlled exceptions.

## Guardrails
Do not build a generic framework before demonstrated need; preserve legitimate low-level access under scoped ownership.
