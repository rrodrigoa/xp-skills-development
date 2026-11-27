# Java dependency injection and composition

## Shared guidance
oo-design: dependency-injection, solid-dip, service-layer

## When to load
Wire services, clocks, repositories or providers.

## Language-specific decisions
Prefer explicit constructor injection with required final collaborators. Wire in an application composition root; when Spring/CDI is already used, keep framework annotations at appropriate boundaries and lifecycle scopes explicit. Use qualifiers only for genuine ambiguity. Avoid pulling dependencies from static context or global application container.

## Verification and evidence
Construct domain/application objects without starting framework when feasible; test scopes, shutdown and alternate implementations.

## Avoid
Field injection that hides mandatory dependencies, service locator or accidental singleton mutable state.
