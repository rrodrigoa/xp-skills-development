# Java boundary and domain validation

## Shared guidance
dev-implementation: models-validation, api-design

## When to load
Parse incoming DTOs, configuration or commands.

## Language-specific decisions
Use explicit validation or approved Jakarta Validation at boundary; annotations alone do not enforce invariants without invoked validation. Domain constructors and operations protect invariants independently. Use typed request DTOs, explicit mapping and separate authorization.

## Verification and evidence
Test invalid fields, cross-field invariants, coercion, unauthorized input and transport-to-domain mapping.

## Avoid
Framework validators as sole business/security enforcement.
