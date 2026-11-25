# Move behavior to owner

## Use when
Feature envy or behavior depends on another object's internals.

## Avoid when
Moving use-case orchestration into an entity.

## Implementation
Move invariant/policy behavior to owner, pass only needed inputs, replace private-field access with behavior; preserve call compatibility if necessary.

## Verification and review
Fewer foreign attribute reads; invariants still protected.
