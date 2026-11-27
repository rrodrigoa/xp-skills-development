# Python naming and layout

## Shared guidance
dev-implementation: naming, module-design

## When to load
Add or rename Python symbols.

## Language-specific decisions
Follow existing PEP 8-based policy: snake_case functions and variables, PascalCase classes, uppercase constants, leading underscore internal names. Prefer is_/has_/can_ predicates, domain terms and explicit units. Keep public keyword arguments and import paths stable unless authorized.

## Verification and evidence
Review public signatures, installed imports and compatibility tests.

## Avoid
Generic Helper/Manager names, shadowing builtins or Java-style getters by habit.
