# Replace conditionals with polymorphism

## Use when
Growing type/strategy switch duplicated across operations.

## Avoid when
Small closed enum dispatch or one simple conditional.

## Implementation
Separate variant policies via protocol or callable, choose once at composition boundary; retain explicit validation and unsupported variant error.

## Verification and review
Add variant without editing every call site; test all branches.
