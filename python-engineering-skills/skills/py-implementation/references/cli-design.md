# CLI architecture

## Use when
Building or extending a command-line tool.

## Avoid when
Business logic inside argparse/Typer callbacks.

## Implementation
Parse arguments into typed request; bootstrap dependencies; call use case; render output separately. Use argparse for stdlib or existing Click/Typer. Stable exit codes, stdout for results, stderr for diagnostics, --help and --version.

## Verification and review
Test programmatic main(argv), subprocess invocation, JSON output, bad args and exit codes.

## Public CLI contract checklist

Document input grammar, defaults, stdout format, stderr diagnostics, exit codes, timeout/cancellation, and whether commands have side effects. For destructive commands consider explicit confirmation or dry-run and noninteractive policy. Use installed console entry points declared under `[project.scripts]`; provide a main entry point that accepts an optional list of argument strings and returns an integer exit status where practical. Do not call sys.exit inside reusable services. Standard argparse uses exit 2 for invalid syntax; choose and document application-specific failure codes. A command must not print a success result if the service failed. For --json, use a stable schema and never mix progress output with JSON.

## Verification matrix

| Case | Expected observation |
|---|---|
| --help | 0, useful usage |
| Valid request | 0, valid output contract |
| Invalid flag | nonzero, actionable diagnostic |
| Domain error | documented nonzero code, no success payload |
| Non-TTY | no unexpected prompt |
| Cancellation | bounded cleanup, no misleading completion |

For a worked design in prose, select the CLI blueprint in `py-migration`.
