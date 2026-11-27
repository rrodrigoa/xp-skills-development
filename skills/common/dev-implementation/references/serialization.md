# Serialization and schemas

## Use when
Persistent or wire formats need compatibility.

## Avoid when
Native object deserialization of untrusted content or implicit internal-field export.

## Implementation
Use explicit versioned serialization and validated schema; UTC timestamps with timezone, stable field names; migrate old payloads deliberately.

## Verification and review
Golden roundtrip, unknown version, backward compatibility and malformed payload tests.
