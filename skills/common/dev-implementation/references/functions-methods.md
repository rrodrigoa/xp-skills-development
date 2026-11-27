# Functions versus methods

## Use when
Choosing location of behavior.

## Avoid when
Class for every function or static-only namespace classes.

## Implementation
Use pure functions for independent transformations; instance methods for owned state or injected collaborators; classmethod for alternate construction; staticmethod only when strongly type-related.

## Verification and review
No implicit globals, artificial self or repeated context argument bundles.
