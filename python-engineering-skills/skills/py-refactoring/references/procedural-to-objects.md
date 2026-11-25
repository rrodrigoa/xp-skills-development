# Procedural-to-object refactoring

## Use when
Functions repeatedly pass mutable context, flags, client and state.

## Avoid when
Moving pure functions to static methods or creating god object.

## Implementation
Cluster functions by invariant and lifecycle; introduce a typed value/state owner; move behavior that owns it; inject I/O as ports; retain compatibility facade as needed; remove redundant functions after callers migrate.

## Verification and review
Compare behavior, reduce context parameters and mutation sites; independent instances cannot interfere.

## Worked example: account lifecycle
A procedural service stores balances in a shared dictionary and passes that dictionary plus an account identifier to every operation. Debit and credit mutate the same value; invalid amounts and insufficient funds must be handled consistently. Introduce an Account entity that owns its balance and enforces those invariants through behavior, rather than exposing a mutable balance. Retain a pure money conversion function if needed. Inject a repository only when persistence is required; the application service coordinates transactions and the adapter translates the old public interface.

Migration order: characterize valid operations, invalid amounts and unknown IDs; introduce the entity; test its invariants; translate old calls through a compatibility facade; migrate callers; remove the old API only when authorized. Constructor validation can reject formerly accepted data, so check compatibility explicitly. Preserve transaction, concurrency and identity guarantees. Verify independent accounts do not share state, and that failed debit leaves the balance unchanged. See the migration skill for the library/service blueprint and dual-path migration.
