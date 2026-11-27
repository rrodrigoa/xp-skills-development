# Anomaly detection and adaptive alerting

## When to load
Considering statistically learned baselines or anomaly alerts.

## Procedure
Define what anomaly predicts and its operational action; distinguish anomaly from SLO breach. Establish representative baseline with seasonality, deployments, traffic changes and data coverage. Choose robust baseline and bounded evaluation windows; consider cold start, concept drift, outliers and contaminated training periods. Backtest against labeled incidents and healthy periods, compare simple thresholds and SLO burn rules, quantify precision/recall with uncertainty and detection latency. Use anomaly as advisory unless independent evidence and policy justify paging. Monitor model health, feature freshness and fallback; retain explainable reason and safe escalation.

## Required evidence and acceptance
Chronological holdout/backtest with known events, false positives, misses, latency, coverage and comparison to simple rule; document drift and rollback.

## Guardrails
Do not claim anomaly equals root cause or train/evaluate on same incident windows without disclosure.
