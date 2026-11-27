# Java Javadoc and comments

## Shared guidance
dev-implementation: comments-docstrings

## When to load
Document public classes, methods and contracts.

## Language-specific decisions
Explain behavior, units, nullability, thread safety, ownership, ordering, exceptions and extension contracts. Use relevant Javadoc tags and links; match supported JDK/doclet. Inherited docs only when substitutable; document changed constraints explicitly and reject weaker contracts.

## Verification and evidence
Generate Javadoc with approved doclint policy and compare against public behavior.

## Avoid
Repeating getters or syntax, stale examples and comments excusing unimplemented requirements.
