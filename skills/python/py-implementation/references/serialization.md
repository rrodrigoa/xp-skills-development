# Python serialization and boundaries

## Shared guidance
dev-implementation: serialization, cross-language-contracts

## When to load
Serialize or exchange persisted data.

## Language-specific decisions
Use versioned explicit JSON/schema mapping or approved codec. Never unpickle untrusted input; avoid implicit __dict__ export. Specify datetime, Decimal, bytes, enum and missing-value representations.

## Verification and evidence
Round-trip and cross-language fixtures with Unicode, numeric precision, malformed data and old versions.

## Avoid
Leaking internal attributes or silent default conversion.
