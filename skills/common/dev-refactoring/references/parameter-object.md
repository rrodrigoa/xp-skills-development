# Introduce parameter object

## Use when
Same related values travel together across APIs.

## Avoid when
Bundling unrelated args into a context bag.

## Implementation
Name meaningful request or domain value, validate invariants, prefer frozen data; migrate callers and remove duplicate parameters.

## Verification and review
Tests confirm validation, defaults and compatibility.
