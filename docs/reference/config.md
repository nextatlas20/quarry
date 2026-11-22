---
id: "config-ref"
title: "Configuration Reference"
owner: "core-runtime"
section: "Reference"
status: "published"
stability: "stable"
---

# Configuration Reference

All keys live under the top-level `quarry.yaml` document.

| Key | Type | Default | Meaning |
| --- | --- | --- | --- |
| `runtime.checkpoint_interval` | duration | `30s` | commit cadence |
| `runtime.dedup_state_budget` | size | `512MB` | per-worker dedup state |
| `runtime.backfill_worker_share` | float | `0.5` | worker share for backfills |
| `coordinator.advertise_addr` | string | none | address agents dial |
| `sink.commit_timeout` | duration | `60s` | sink commit deadline |

Unknown keys are rejected at startup; `quarry doctor --strict` reports them
before a run starts.
