# Characterization tests and safe baseline

## Use when
Legacy behavior is unclear or untested.

## Avoid when
Treating accidental bugs as permanent without review.

## Implementation
Capture representative inputs, outputs, side effects, exceptions and ordering; record known defects separately. Run baseline before changes, preserve behavior unless approved.

## Verification and review
Old and new implementations pass same contract; approved fixes have regression tests.
