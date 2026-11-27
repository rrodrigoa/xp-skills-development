# Python visibility and descriptors

## Shared guidance
oo-design: object-model, package-boundaries

## When to load
Protect state and published interfaces.

## Language-specific decisions
Use leading underscore for internal members; properties for computed or read-only exposure; name mangling is not security. Keep public exports intentional, avoid import-time I/O and cycles. Use composition rather than metaclass or descriptor machinery unless necessary.

## Verification and evidence
Inspect public imports from installed artifact, test state mutation through public API and verify import side effects.

## Avoid
Exposing mutable internals or treating private naming as authorization.
