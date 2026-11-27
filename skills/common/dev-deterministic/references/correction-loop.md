# Convert repeated feedback into enforcement

## When to load
A reviewer or user corrects an agent.

## Implementation in the target project
Write a correction record with concrete failing example, desired behavior, scope, reason and owner. Determine if the failure is mechanical, behavioral, architectural or intent-dependent. Reproduce it before repair; design an API restriction or targeted checker and include legitimate exceptions. Migrate existing occurrences or baseline them. Run the good/bad fixtures, check existing callers and propose independent approval. Replace repetitive prose with a concise pointer to diagnostic guidance.

## Required evidence and acceptance
A new violation fails the same local and CI check; a valid alternative passes; rule owner and scope are recorded. Confirm the fix did not conceal the original symptom.

## Guardrails
A single preference is not necessarily a universal policy. Avoid overfitting a rule to one syntax or one model output.
