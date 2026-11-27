# Browser and desktop UI verification

## When to load
User-facing workflow or UI changes.

## Implementation in the target project
Use approved browser/desktop driver such as Playwright or CDP where supported; select controls by accessible role/name or explicit test IDs. Wait for meaningful state rather than arbitrary sleeps. Assert text, enabled state, persistence, error feedback, focus, keyboard and relevant responsive behavior. Exercise cancellation, retries and reload where applicable; capture console/network failures and trace. For Electron verify main/renderer boundary and packaged app when required.

## Required evidence and acceptance
Scripted user journey passes expected assertions, invalid path fails correctly, artifacts link to exact candidate and environment.

## Guardrails
Visual inspection helps but is not proof of all functionality. Browser automation alone may not cover native dialogs or OS integration.
