# Public API and compatibility

## Use when
A library exposes types or methods to other callers.

## Avoid when
Exporting every internal helper.

## Implementation
Define documented import paths and contracts, use explicit exports where useful, version changes and maintain deprecation periods appropriate to project.

## Verification and review
Test public imports from built wheel and existing callers.
