# Negative and adversarial tests

## Use when
Untrusted inputs, permissions, files, tools or network boundaries.

## Avoid when
Only happy-path coverage or live attack against unauthorized systems.

## Implementation
Test malformed schema, path traversal, unauthorized operations, injection strings, resource limits and secret redaction in isolated fixtures. Assert rejection before side effects.

## Verification and review
Verify forbidden actions did not occur; allowed controls still succeed.
