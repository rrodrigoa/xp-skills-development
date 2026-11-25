# Serialization and schemas

## Use when
Persistent or wire formats need compatibility.

## Avoid when
Pickle for untrusted content or implicit __dict__ export.

## Implementation
Use explicit versioned serialization and validated schema; UTC timestamps with timezone, stable field names; migrate old payloads deliberately.

## Verification and review
Golden roundtrip, unknown version, backward compatibility and malformed payload tests.
