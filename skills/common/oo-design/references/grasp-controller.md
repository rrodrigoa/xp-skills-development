# GRASP Controller

## When to load
Multiple entry points initiate the same use case.

## Design procedure
A controller receives a system event and delegates to the application use case. It is not necessarily a web controller; a CLI command, agent tool, or message handler can play this role. Keep transport decoding, authorization at the boundary, and result translation distinct from business decisions. Define a typed request/result and injected collaborators; avoid passing framework request objects into the domain. Use one use-case controller per cohesive operation or related set, not one giant controller for every feature.

## Verification
Drive the same use case through representative entry points and test its behavior without the transport. Verify error, authentication and cancellation mappings.

## Avoid
Duplicating business rules in CLI, API and MCP adapters or treating an HTTP route as the domain service.
