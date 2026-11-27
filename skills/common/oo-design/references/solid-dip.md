# Dependency inversion

## Use when
Business code imports concrete SDKs, databases or framework adapters.

## Avoid when
Pure helpers or stable standard-library value types.

## Implementation
Define ports near their consumer; inject adapters at composition root; avoid global service locators.

## Verification and review
Domain imports no infrastructure; tests substitute an adapter without monkeypatching globals.
