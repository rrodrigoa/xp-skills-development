# Bridge

## Use when
Two independent axes of variation would multiply subclasses.

## Avoid when
Only one axis varies.

## Implementation
Compose abstraction with implementation protocol; keep each axis independently extensible.

## Verification and review
Test combinations across both axes without new subclasses.

## Refactoring recipe
**Trigger:** Independent transport and operation variations create a subclass cross product.

**Migration:** Identify two axes and contracts; extract one axis as injected collaborator, retain old combinations via composition, then simplify subclasses.

**Acceptance:** Test supported cross combinations and independent extension of each axis.

**Tradeoff:** Use one strategy if only one variation axis exists.
