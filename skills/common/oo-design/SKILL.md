---
name: oo-design
description: "Design object models, boundaries, SOLID, dependency injection, modular packages, domain and service layers."
---
# Architecture

Inspect responsibilities and data flow. Identify domain concepts, invariants, lifecycle, callers and external dependencies. Select the smallest architecture that protects those boundaries. Use typed values and behavior-owning objects for meaningful state; use pure functions where appropriate. Document significant dependency decisions with an ADR. Do not introduce layers with no independent responsibility. Verify dependency direction and contract behavior.

## Reference selector
Read only relevant files from this list.

- [Object modeling and responsibilities](references/object-model.md) — Multiple operations manipulate the same state, invariants or lifecycle.
- [Single responsibility](references/solid-srp.md) — One module changes for unrelated business, persistence and presentation reasons.
- [Open/closed principle](references/solid-ocp.md) — New variants repeatedly require edits to stable dispatch logic.
- [Liskov substitution](references/solid-lsp.md) — Several implementations claim one interface.
- [Interface segregation](references/solid-isp.md) — Consumers depend on unrelated operations or mocks implement many unused methods.
- [Dependency inversion](references/solid-dip.md) — Business code imports concrete SDKs, databases or framework adapters.
- [Composition, delegation and inheritance](references/composition-inheritance.md) — Behavior needs reuse or interchangeable collaborators.
- [Value objects and entities](references/value-objects.md) — Primitive values carry units, validation or identity.
- [Interfaces and abstract base types](references/protocols-abcs.md) — Multiple implementations or external boundaries need a contract.
- [Dependency injection and composition root](references/dependency-injection.md) — Services need storage, clock, transport or policy.
- [Layered and hexagonal architecture](references/layered-hexagonal.md) — Domain logic coupled to frameworks and external systems.
- [Module and package boundaries](references/package-boundaries.md) — Large package has circular imports or incoherent utils modules.
- [Application service and use cases](references/service-layer.md) — Multiple entry points need the same business operation.
- [DDD aggregates and invariants](references/aggregate.md) — Multiple entities must change consistently within a transaction.
- [Repository and unit of work](references/repository-uow.md) — Domain objects need persistence and atomic changes.
- [Architecture decision records](references/adr.md) — A consequential tradeoff changes dependencies, contracts or operations.
- [Modular monolith vs services](references/modular-monolith.md) — Features have distinct ownership and independent evolution.
- [Public API and compatibility](references/public-api.md) — A library exposes types or methods to other callers.

For graph evidence, metrics and enforceable architecture contracts, use `dev-architecture-analysis`. For a staged conversion from existing designs, use `dev-migration`.

- [Behavioral objects versus data carriers](references/behavior-vs-data.md) — Load for this specific topic.

- [GRASP Information Expert and Creator](references/grasp-information-expert.md) — Choosing responsibility owners and object construction.

- [GRASP Low Coupling and High Cohesion](references/grasp-coupling-cohesion.md) — Assessing responsibility concentration and dependency fragility.

- [GRASP Controller](references/grasp-controller.md) — Separating entry-point handling and application use cases.

- [GRASP Polymorphism and Protected Variations](references/grasp-polymorphism.md) — Selecting polymorphism and isolating volatile dependencies.

- [GRASP Pure Fabrication and Indirection](references/grasp-indirection.md) — Extracting technical responsibilities without gratuitous wrappers.

- [Tell, do not ask and Law of Demeter](references/tell-dont-ask.md) — Preventing feature envy and internal graph leakage.
