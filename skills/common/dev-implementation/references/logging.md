# Logging and diagnostics

## Use when
Library or tool needs actionable diagnostics.

## Avoid when
print debugging, log-and-reraise duplication or secret dumps.

## Implementation
Use module logger; applications configure sinks; structured fields with correlation IDs; levels reflect actionability; avoid eager expensive formatting.

## Verification and review
Capture logs and assert redaction and correct severity.
