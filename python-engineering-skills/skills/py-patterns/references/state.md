# State

## Use when
Behavior varies by lifecycle state and transitions are complex.

## Avoid when
Few stable transitions fit a small enum and table.

## Implementation
Encapsulate state-specific behavior or use typed transition table; owner enforces legal transitions and persistence.

## Verification and review
Test all legal and illegal transitions and terminal behavior.

## Refactoring recipe
**Trigger:** Behavior switches repeatedly on lifecycle enum or flags.

**Migration:** Map transitions and state-specific operations; preserve explicit state machine first, introduce state objects only if behavior complexity warrants, move branches incrementally.

**Acceptance:** Test every legal transition, forbidden transition, failures and persisted state compatibility.

**Tradeoff:** Simple enum with transition table may be sufficient; avoid subclass for each trivial state.
