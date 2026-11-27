# Adapter

## Use when
An external interface differs from a consumer-owned port.

## Avoid when
Both interfaces already match.

## Implementation
Translate data, exceptions and semantics at boundary; delegate to adaptee; keep domain independent of vendor types.

## Verification and review
Contract tests include error translation and unsupported capabilities.

## Refactoring recipe
**Trigger:** Domain or service directly calls a provider with incompatible types or errors.

**Migration:** Characterize provider calls, define consumer-owned contract, implement translation for existing provider, switch callers and remove leaked SDK types from public core.

**Acceptance:** Shared contract tests, translation of errors, timeout and cancellation, no provider import in domain.

**Tradeoff:** Do not wrap an already matching interface without a reason.
