# Reusable generation specification

## When to load
Instructing an agent to generate a reusable component or project slice.

## Procedure
Specify input requirements, supported language and runtime versions, public contracts, responsibilities, dependency graph, lifecycle, error model, configuration, security, tests and required docs. Identify allowed extension points and explicitly excluded scope. Reuse existing conventions first and ask the agent to implement in the target repo only.

## Required evidence and acceptance
Deliver a prose design manifest with named artifacts and acceptance tests; independently review generated output against it.

## Guardrails
No source template or generator in this repository. No invented framework, dependency or default transport; avoid scaffolding empty layers.
