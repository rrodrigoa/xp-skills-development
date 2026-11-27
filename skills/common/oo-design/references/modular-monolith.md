# Modular monolith vs services

## Use when
Features have distinct ownership and independent evolution.

## Avoid when
Splitting a deployment only because files are large.

## Implementation
Establish module APIs and ownership first; use processes/services only for justified deployment, scaling or isolation needs.

## Verification and review
Verify no cross-module private imports; document operational cost.
