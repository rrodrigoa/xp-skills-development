# Cross-language contracts

## When to load
A Python, Java or other component calls another process, service, native library or generated client.

## Procedure
Define one authoritative versioned schema with required/optional values, null versus missing, units, numeric precision and ranges, enum evolution, time zones, error mapping, correlation and authentication. Establish ownership of serialization, timeout, retry and idempotency. Define wire encoding, framing, maximum sizes, ordering and cancellation. Use boundary adapters rather than leaking foreign framework types into domain models. Record supported producer/consumer version combinations and rollout order. Test generated clients and hand-written adapters against the same fixtures.

## Evidence
Run cross-language round-trip, contract and mixed-version tests against actual artifacts. Include unknown fields, invalid inputs, Unicode, precision, timeouts, unauthorized requests and partial failures. Verify neither side treats an error as success. Report untested combinations as unknown. Avoid duplicating business rules across languages unless ownership and synchronization are explicit.
