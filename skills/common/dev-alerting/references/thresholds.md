# Threshold selection, windows and hysteresis

## When to load
Designing static or dynamic alert conditions.

## Procedure
Use approved SLO or capacity constraints first; calibrate other thresholds with historical healthy/degraded data, seasonality, traffic volume and response time. Define aggregation, window, evaluation cadence, pending duration and recovery threshold or keep-firing interval where supported. Account for scrape/evaluation delays and rule semantics; test single spikes, sustained degradation, intermittent breaches and flapping. Use dynamic baselines only with adequate history, seasonality handling and explainable false-positive/negative rates; keep a hard safety bound when justified. Document why each condition changes an operational decision.

## Required evidence and acceptance
Backtest on known incidents and normal periods; report detection delay, misses, false notifications and recovery behavior before activation.

## Guardrails
Do not tune thresholds solely to reduce pages or confuse dashboard display thresholds with backend rules.
