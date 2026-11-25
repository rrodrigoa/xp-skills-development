# Agent evaluations and regression gates

## Use when
Prompts, tools, model, routing, orchestration or policies change. This card defines evaluation guidance only.

## Procedure
Define task ID, versioned inputs, environment, model, permissions, expected observable outcomes, allowed and forbidden tool actions, and independent evidence. Include positive, negative, adversarial, ambiguous, failure and multi-turn cases as applicable. Separate deterministic outcome checks from calibrated semantic rubrics. Run equivalent baseline and candidate conditions with repetitions and record uncertainty. Score each criterion separately (0 absent, 1 partial, 2 demonstrated; UNKNOWN for missing evidence). Count unauthorized effects, fabricated results, missed required denials and manipulated checks as hard failures where policy applies.

## Verification and review
Report per-scenario outcomes, observed calls and side effects, hallucinations, latency, cost, variance, model and configuration. Gate only using an approved threshold and `py-quality-gates` AI-01; a high average score cannot excuse an applicable hard failure. Use `py-governance` for calibration and approval. No harness is included; never claim evaluations ran from prose alone.
