# Semantic migrations and invariant changes

## When to load
Changing behavior ownership or representation across modules.

## Procedure
List old and new invariants, data shape, errors, side effects, ordering and transaction semantics. Identify compatibility adapters, conversion rules and unsupported states. Characterize boundary behavior before converting each caller. Obtain authorization for intentional behavioral change.

## Required evidence and acceptance
Old/new contract matrix, caller inventory, tests of valid/invalid states and failure paths; explicit decision for any intentional difference.

## Guardrails
Do not describe a behavior change as mere refactoring. Data conversion may be lossy; require recovery plan and ownership.
