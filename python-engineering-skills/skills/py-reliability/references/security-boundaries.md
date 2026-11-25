# Security and trust boundaries

## Use when
Processing user input, network, files or plugins.

## Avoid when
Trusting internal-looking strings or model outputs.

## Implementation
Validate at boundary, authorize action separately, default deny sensitive operations, use least privilege, parameterized queries and safe APIs; avoid shell=True for untrusted strings.

## Verification and review
Negative tests show rejection and no side effects; audit logs redact secrets.
