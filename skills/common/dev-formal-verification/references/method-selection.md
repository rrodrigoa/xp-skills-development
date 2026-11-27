# Choose the right verification method

## When to load
High-risk invariant or complex algorithm.

## Implementation in the target project
Identify claim, system boundary, state space, quantification and failure cost. Use executable tests for concrete behavior, property tests for sampled input spaces, model checking for finite abstract transitions, theorem proving for mathematical statements, and static analysis for syntactic/type properties. Select method by claim and cost; define implementation correspondence and complementary tests.

## Required evidence and acceptance
Verification plan names property, method, assumptions, scope, tool and expected evidence. Unverified claims remain explicit.

## Guardrails
Formal techniques do not guarantee product intent or correctness outside the modeled assumptions.
