# Dependency management and reproducibility

## Use when
Adding dependencies or deploying.

## Avoid when
Adding package for trivial functionality or pinning library transitive deps indiscriminately.

## Implementation
Evaluate maintenance, security, license and footprint; declare direct runtime vs dev deps; lock application/dev environments per toolchain; support documented runtime range.

## Verification and review
Resolve clean environment, audit dependencies, check optional extras.
