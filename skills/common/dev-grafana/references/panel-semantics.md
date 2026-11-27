# Panel visualization, transformations and units

## When to load
Selecting visualization or debugging misleading charts.

## Procedure
Use time series for trends, stat for explicitly reduced current/window value, table for ranked/cohort detail, histogram/heatmap for distributions and state timeline for discrete transitions. Specify reducer (last, max, sum, count or other) and time range; show sample count when interpreting tail statistics. Match units to source and conversion, format ratios consistently, avoid misleading axes and distinguish thresholds from SLO. Transformations may join, reduce or filter data; check keys, timestamp alignment, nulls and row loss. Display fresh zero, stale and absent distinctly. Compare final panel data with raw datasource query before trusting rendering.

## Required evidence and acceptance
Test known values, nulls, mismatched joins, different time ranges and threshold boundaries; document intended meaning of each reducer.

## Guardrails
Do not use display transformations to repair incorrect measurement semantics or assume dashboard transforms apply to alert evaluation.
