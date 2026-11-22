---
id: "dedup"
title: "Record Deduplication"
owner: "analytics-eng"
section: "Guides"
status: "published"
stability: "beta"
---

# Record Deduplication

Deduplication keeps the newest record per key inside a bounded window.

```yaml
transforms:
  - kind: dedup
    keys: [event_id]
    order_by: ingest_time
    window: 6h
```

## Window semantics

Records are held in coordinator state until the window closes. A window of six
hours therefore permits late duplicates up to six hours old; anything older is
forwarded unchanged.

## Memory budget

State is spilled to disk when it exceeds `runtime.dedup_state_budget` (default
512 MB per worker).
