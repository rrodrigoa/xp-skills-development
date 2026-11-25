# Subprocess and terminal execution

## Use when
CLI invokes other programs.

## Avoid when
Unbounded waits, shell interpolation or inherited secrets.

## Implementation
Pass argv list, shell=False, explicit cwd/environment, timeout and bounded output; define process tree cancellation per OS; never execute untrusted code without isolation.

## Verification and review
Test nonzero exit, timeout, spaces, cancellation and output limits.
