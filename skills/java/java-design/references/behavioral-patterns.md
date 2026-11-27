# Java behavioral patterns

## Shared guidance
oo-patterns: strategy, command, observer, iterator, visitor, state, interpreter, mediator, memento, template-method, chain-of-responsibility

## When to load
Select dispatch, event delivery or workflow representation.

## Language-specific decisions
Prefer functional interfaces and method references for simple strategies/commands; classes when state/lifetime matters. Use Iterator/Iterable and stream traversal with explicit consumption semantics. Use sealed hierarchy plus exhaustive switch where supported and alternatives closed; visitor for stable extensible operations on a known hierarchy. Use explicit listener lifecycle and bounded queues; avoid deprecated Observable.

## Verification and evidence
Test all variants, listener failures, cancellation, single-use streams, illegal transitions and memento isolation.

## Avoid
Pattern boilerplate where an enum or pure function suffices; hidden stream side effects.
