# Extract method/function

## Use when
Long routine has distinct named steps.

## Avoid when
Extracting tiny wrappers solely to reduce line count.

## Implementation
Identify coherent block with clear input/output; name by purpose; keep domain ownership; avoid parameter explosion.

## Verification and review
Existing tests pass; extracted unit readable in isolation.
