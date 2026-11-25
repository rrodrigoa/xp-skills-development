# Protocols versus abstract base classes

## Use when
Multiple implementations or external boundaries need a contract.

## Avoid when
A concrete internal type has no meaningful substitution.

## Implementation
Use typing.Protocol for structural interfaces; ABC when nominal membership or shared lifecycle is essential. Do not mistake runtime_checkable for signature validation.

## Verification and review
Static check plus behavioral contract tests.
