# Java nullability and Optional

## Shared guidance
dev-implementation: models-validation, errors

## When to load
Clarify absent values and boundary validation.

## Language-specific decisions
Use explicit nullability policy and approved annotations/checker; validate required values at construction and boundary. Optional can express absence in return values; avoid blanket Optional fields or parameters unless contract warrants it. Distinguish absent, null, empty and invalid in wire mappings.

## Verification and evidence
Test null, missing, empty and default paths; verify checker coverage and error contract.

## Avoid
Returning null from Optional API, indiscriminate Optional.get or masking invalid inputs with defaults.
