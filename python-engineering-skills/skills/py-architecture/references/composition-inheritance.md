# Composition, delegation and inheritance

## Use when
Behavior needs reuse or interchangeable collaborators.

## Avoid when
Inheritance merely to share code.

## Implementation
Prefer injected collaborators; inherit when there is a genuine substitutable is-a relationship and a stable base contract. Keep hierarchy shallow and super calls intentional.

## Verification and review
Test substitution and independent collaborator replacement.
