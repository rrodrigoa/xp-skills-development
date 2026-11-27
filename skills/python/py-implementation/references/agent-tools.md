# Python agent and MCP adapter implementation

## Shared guidance
dev-agent-systems: mcp-tools, llm-adapters, structured-output; dev-implementation: api-design

## Language-specific decisions
Use typed request/result contracts and Pydantic or explicit boundary validation where approved. Keep MCP/LLM SDK objects in adapters; route authorized requests into reusable application use cases. Handle async SDK lifetime and cancellation with deterministic scopes; avoid blocking an async event loop. Select SDK and protocol version from project dependencies, not assumed newest examples. Validate model-provided tool arguments independently and map errors without exposing secrets.

## Evidence
Use deterministic provider fakes and protocol-level integration tests; test malformed calls, unauthorized operations, timeout, cancellation, structured output validation and actual registered tool schema. Separate model evaluation results from ordinary code tests.

## Avoid
Putting business rules in decorated MCP callbacks or treating model-generated arguments as trusted.
