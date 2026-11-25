# Interpreter

## Use when
A small controlled grammar needs compositional evaluation.

## Avoid when
General-purpose language or complex grammar better served by parser library.

## Implementation
Model typed syntax tree nodes and explicit evaluator; parse and validate separately; never use eval on untrusted text.

## Verification and review
Test grammar, precedence, invalid nodes and depth limits.

## Refactoring recipe
**Trigger:** Repeated ad hoc parsing and evaluation of small expression language.

**Migration:** Specify grammar and semantics; separate parse, validated syntax tree and evaluation; replace existing branches incrementally and retain accepted syntax.

**Acceptance:** Test precedence, invalid syntax, unknown names, resource limits and injection rejection.

**Tradeoff:** Use established parser for larger grammars; never evaluate arbitrary user code.
