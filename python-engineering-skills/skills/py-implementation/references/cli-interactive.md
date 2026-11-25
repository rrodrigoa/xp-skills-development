# Interactive and machine-readable CLI

## Use when
Tool used by humans and agents.

## Avoid when
Progress bars or prompts corrupting stdout JSON.

## Implementation
Support --json, --no-input and non-TTY detection when needed. Send progress to stderr; do not prompt in noninteractive mode. Return documented structured errors, handle cancellation.

## Verification and review
Pipe stdout to parser, test EOF, non-TTY and Ctrl-C cleanup.
