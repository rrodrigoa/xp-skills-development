# LLM provider adapter

## Use when
Multiple OpenAI-compatible or other LLM endpoints.

## Avoid when
Provider details spread through domain logic.

## Implementation
Define typed request/result and protocol; inject provider; normalize errors, timeouts, streaming and tool-call validation; model capabilities explicit.

## Verification and review
Contract tests with stub and optional live endpoints; no hidden fallback.
