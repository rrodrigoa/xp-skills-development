# Java agent and MCP adapter implementation

## Shared guidance
dev-agent-systems: mcp-tools, llm-adapters, structured-output; dev-implementation: api-design

## Language-specific decisions
Use typed request/result records or validated DTOs and explicit mapping into application services. Keep the selected MCP/LLM SDK and framework types in adapters; confirm protocol and SDK compatibility with the project's JDK. Choose blocking, CompletionStage or reactive APIs according to actual SDK and runtime; propagate cancellation, timeouts and correlation across boundaries. Validate tool arguments and authorization before side effects; reject unsupported provider capabilities instead of silently degrading.

## Evidence
Use deterministic provider doubles and actual registered-tool contract tests, including malformed inputs, unsupported calls, permission failures, timeouts, cancellation and structured result mapping. Verify resource shutdown and tool schema against the selected SDK version.

## Avoid
Putting domain rules inside annotations/callbacks, blocking reactive event loops or assuming generated JSON schema enforces authorization.
