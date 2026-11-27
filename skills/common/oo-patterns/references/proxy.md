# Proxy

## Use when
Control access, lazy creation or remote access while preserving interface.

## Avoid when
Simple direct access or unrelated behavior.

## Implementation
Implement same port, guard or lazily acquire delegate; define synchronization, failure and lifecycle.

## Verification and review
Test unauthorized access, lazy creation and contract preservation.

## Refactoring recipe
**Trigger:** Consumers need controlled access, lazy initialization or remote behavior behind existing interface.

**Migration:** Define semantics including authorization, latency and failure; insert proxy around target, preserve interface, configure at composition root.

**Acceptance:** Test denial without target invocation, initialization concurrency, timeout and remote errors.

**Tradeoff:** Do not pretend remote failure semantics equal local calls; no bypass path for required controls.
