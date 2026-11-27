# Contract tests

## Use when
Multiple implementations, versioned APIs or MCP tools.

## Avoid when
Duplicating all implementation tests in each adapter.

## Implementation
Define common behavioral suite with adapter factories; cover errors, edge cases, ordering and lifecycle; compare compatibility schema.

## Verification and review
Run same suite for every supported adapter.
