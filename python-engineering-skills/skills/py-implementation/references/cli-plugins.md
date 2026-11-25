# CLI plugins and extension points

## Use when
Third parties add commands or backends.

## Avoid when
Dynamic discovery for a closed internal command set.

## Implementation
Use explicit registry first; for external packages use importlib.metadata entry points with documented protocol, duplicate-name policy and trust model. Load only selected plugins where possible.

## Verification and review
Test missing, incompatible and duplicate plugins; never auto-execute untrusted code.
