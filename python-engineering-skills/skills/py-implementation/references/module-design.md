# Module cohesion and reuse

## Use when
Similar helpers appear across modules.

## Avoid when
Premature shared utilities or generic frameworks.

## Implementation
Search existing code first; extract a shared abstraction only when semantics match. Keep dependencies explicit and public surface minimal; no catch-all utils module.

## Verification and review
Two consumers use same coherent contract; no circular imports.
