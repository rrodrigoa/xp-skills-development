---
name: oo-patterns
description: "Select and implement classic OO and enterprise patterns across languages; compare alternatives and avoid unnecessary abstractions."
---
# Object-Oriented and Enterprise Patterns

Identify actual variation, ownership, lifecycle or coupling before selecting a pattern. Use the catalog below by intent; load only the candidate reference and competing reference if needed. Prefer idioms of the selected language over mechanical translations; load the applicable language design skill. A named pattern is not a requirement: justify it by a concrete problem. Pattern cards include prose migration recipes and verification criteria; implement only in the target project.

## Reference selector
Read only relevant files from this list.

- [Abstract Factory](references/abstract-factory.md) — A family of compatible products must vary together.
- [Builder](references/builder.md) — Construction has ordered steps or many optional values with final validation.
- [Factory Method](references/factory-method.md) — A base workflow needs a customizable product creation hook.
- [Prototype](references/prototype.md) — Create independent objects from configured exemplars.
- [Singleton](references/singleton.md) — Exactly one resource per explicit scope is required.
- [Adapter](references/adapter.md) — An external interface differs from a consumer-owned port.
- [Bridge](references/bridge.md) — Two independent axes of variation would multiply subclasses.
- [Composite](references/composite.md) — Tree of objects needs uniform operations across leaves and groups.
- [Decorator](references/decorator.md) — Add independently composable behavior around the same interface.
- [Facade](references/facade.md) — Consumers need a simple entry point to a complex subsystem.
- [Flyweight](references/flyweight.md) — Many objects repeat immutable intrinsic state causing measured memory cost.
- [Proxy](references/proxy.md) — Control access, lazy creation or remote access while preserving interface.
- [Chain of Responsibility](references/chain-of-responsibility.md) — Multiple handlers may handle or pass a request.
- [Command](references/command.md) — Actions must be represented as values for queueing, history or execution policy.
- [Interpreter](references/interpreter.md) — A small controlled grammar needs compositional evaluation.
- [Iterator](references/iterator.md) — Consumers traverse a collection without depending on storage.
- [Mediator](references/mediator.md) — Components are tightly coupled through many peer interactions.
- [Memento](references/memento.md) — Snapshot/restore internal state for undo or checkpoint.
- [Observer](references/observer.md) — Multiple consumers need notification of changes.
- [State](references/state.md) — Behavior varies by lifecycle state and transitions are complex.
- [Strategy](references/strategy.md) — Algorithm varies independently of its caller.
- [Template Method](references/template-method.md) — A stable workflow has a few well-defined variation hooks.
- [Visitor](references/visitor.md) — New operations frequently target a stable set of node types.
- [Repository](references/repository.md) — Domain needs collection-like persistence.
- [Unit of Work](references/unit-of-work.md) — Several writes need one atomic transaction.
- [Null Object](references/null-object.md) — Optional collaborator has legitimate no-op semantics.
- [Specification](references/specification.md) — Domain predicates need composition and reuse.
- [Registry](references/registry.md) — Known plugins or strategies are selected by name.
- [Object Pool](references/object-pool.md) — Expensive limited reusable resources need bounded checkout.
- [Transactional Outbox](references/outbox.md) — Database change and message intent must be atomic.
- [CQRS](references/cqrs.md) — Read and write models have genuinely different needs.
- [Explicit state machine](references/state-machine.md) — Workflow requires auditable transitions.
- [Pipeline and middleware](references/pipeline.md) — Ordered composable stages process a value.
- [Saga and compensation](references/saga.md) — Cross-service long-lived operations cannot use one transaction.
- [Circuit Breaker](references/circuit-breaker.md) — Repeated remote failures waste capacity.

## Language mapping
This catalog owns pattern intent, applicability, migration and acceptance. For Python, load `py-design` and its relevant pattern-mapping card. For Java, load `java-design` and its relevant pattern-mapping card. Do not duplicate the canonical recipe or force a class-based implementation when a native callable or closed variant is simpler.
