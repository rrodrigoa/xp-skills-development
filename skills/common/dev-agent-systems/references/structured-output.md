# Structured model output

## Use when
Model emits tool args, plans or JSON.

## Avoid when
Treating syntactically valid JSON as authorized or correct.

## Implementation
Use schema constraints when available, validate locally and reject unknown fields as contract requires; bounded correction attempts; distinguish parse and domain errors.

## Verification and review
Test truncation, malformed JSON, hallucinated fields and unauthorized actions.
