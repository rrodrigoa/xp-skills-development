# Java CLI and command entry points

## Shared guidance
dev-implementation: cli-design, cli-interactive; dev-migration: blueprint-cli

## When to load
Create CLI or automation-friendly command.

## Language-specific decisions
Use existing parser or Picocli if approved; parse typed request, compose services, render result outside domain. Return status from testable command handler and call System.exit only at outermost process boundary. Keep stdout machine-readable and stderr diagnostic; handle noninteractive mode, EOF and cancellation.

## Verification and evidence
Test installed JAR/launcher, invalid args, exit codes, stdout schema, stderr and interruption.

## Avoid
Business logic in main or parser callbacks, hard-coded environment assumptions.
