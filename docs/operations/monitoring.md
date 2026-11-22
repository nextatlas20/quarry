---
id: "monitoring"
title: "Monitoring Pipelines"
owner: "sre"
section: "Operations"
status: "published"
stability: "stable"
---

# Monitoring Pipelines

Every coordinator exposes Prometheus metrics on `:9109/metrics`.

## Signals to watch

- `quarry_run_lag_seconds` — distance between the newest record and wall clock
- `quarry_batch_duration_seconds` — p99 latency per batch
- `quarry_checkpoint_failures_total` — non-zero means the sink is rejecting commits

## Suggested alerts

| Alert | Condition |
| --- | --- |
| RunLagHigh | `quarry_run_lag_seconds > 900` for 10m |
| CheckpointFailing | `increase(quarry_checkpoint_failures_total[15m]) > 0` |

Dashboards ship in `contrib/dashboards/` and expect the default job label
`quarry-coordinator`.
