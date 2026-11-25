# Object modeling and responsibilities

## Use when
Multiple operations manipulate the same state, invariants or lifecycle.

## Avoid when
Stateless calculation with no meaningful ownership.

## Implementation
Identify entity, value, policy and collaborator. Give each object a clear responsibility and put invariant-changing operations on its owner. Use private implementation attributes, public behavior and constructor validation; avoid getters/setters that bypass invariants.

## Verification and review
Test invalid construction, valid transitions, illegal transitions and independent instances.

## Responsibility discovery checklist

- List state variables and all writers. Group writers that must preserve the same invariant; they are candidates for one state owner.
- Identify policies that change independently of state. A policy might be a pure function, strategy object or a typed callable.
- Identify long-lived collaborators (storage, model provider, clock, transport, executor). Inject them once into the component that needs them rather than passing a kitchen-sink context through every call.
- Identify public use cases and external actors. Separate input parsing, domain rules and output formatting; preserve the public contract.
- Sketch dependency direction and lifecycle before implementing a subsystem. A simple ownership table is sufficient for a small change.

| Concept | Suggested representation |
|---|---|
| Stable domain value with invariants | Frozen dataclass or small immutable class |
| Identity and mutable lifecycle | Entity with behavior and explicit transitions |
| Varying algorithm | Callable or Strategy protocol |
| External capability | Consumer-owned port and adapter |
| Shared use-case orchestration | Application service with constructor-injected ports |
| Independent calculation | Typed pure function |

Do not infer classes from nouns alone. A class should own a responsibility or abstraction; a module is also a valid encapsulation boundary. No mandatory class/function ratio.
