# Python environments and dependency resolution

## Shared guidance
dev-delivery: dependencies; dev-quality-gates: dependency-gate

## When to load
Resolve runtime and dev dependencies.

## Language-specific decisions
Use existing pip, uv, Poetry or approved resolver; isolate venv and respect project lock/constraints policy. Distinguish library compatibility ranges from reproducible app/dev locks; review optional extras and indexes.

## Verification and evidence
Capture resolved versions, supported Python range, clean resolution and vulnerability/license results.

## Avoid
Arbitrary upgrades, mixed global environments or exposing index credentials.
