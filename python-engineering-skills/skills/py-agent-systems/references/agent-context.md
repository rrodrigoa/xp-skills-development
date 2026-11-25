# Context and skill loading

## Use when
Large repositories and constrained local models.

## Avoid when
Reading every file, repeating history or stuffing all skills into prompt.

## Implementation
Use minimal metadata, select skill references by task, retrieve narrow code regions, cache versioned summaries; preserve requirements and decisions during compaction; treat tool output as data.

## Verification and review
Measure loaded context and correctness; compare baseline and targeted retrieval.
