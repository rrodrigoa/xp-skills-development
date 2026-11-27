# Java exception and error mapping

## Shared guidance
dev-implementation: errors

## When to load
Choose checked/unchecked exceptions and translate failures.

## Language-specific decisions
Follow established API contract; checked exceptions for recoverable obligations where appropriate, unchecked for programming errors and domain failures per policy. Preserve cause on translation; never catch Throwable as routine recovery. On interrupted waits propagate interruption or restore interrupt flag when translating. Use try-with-resources for deterministic cleanup.

## Verification and evidence
Test cause, mapping, suppressed exceptions, interrupt handling, partial initialization and redaction.

## Avoid
Swallowed exceptions, logging and returning success, broad catch masking programmer errors.
