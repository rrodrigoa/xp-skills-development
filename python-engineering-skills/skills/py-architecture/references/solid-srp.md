# Single responsibility

## Use when
One module changes for unrelated business, persistence and presentation reasons.

## Avoid when
Splitting a small cohesive feature into arbitrary classes.

## Implementation
Group by reason to change; split policy, storage and UI at real seams. Keep the use-case coordinator responsible for orchestration only.

## Verification and review
A storage change should not require a domain-policy edit.
