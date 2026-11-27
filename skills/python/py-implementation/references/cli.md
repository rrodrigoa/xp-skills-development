# Python CLI and entry points

## Shared guidance
dev-implementation: cli-design, cli-interactive; dev-migration: blueprint-cli

## When to load
Implement or refactor CLI.

## Language-specific decisions
Use argparse or existing Click/Typer, map parsed args into a typed request, return a status from a testable main function, terminate only at process boundary. Declare installed console scripts under project metadata. argparse commonly exits 2 on invalid arguments; explicitly document project-specific outcomes.

## Verification and evidence
Test installed entry point, stdout JSON, stderr, invalid args, EOF, non-TTY, interrupt and exit status.

## Avoid
Business rules in parser callbacks or sys.exit inside reusable services.
