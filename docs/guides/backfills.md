---
id: "backfills"
title: "Backfill Runs"
owner: "operations"
section: "Guides"
status: "published"
stability: "experimental"
---

# Backfill Runs

A backfill replays a historical range into an existing sink.

```bash
quarry backfill --pipeline events-to-parquet \
  --from 2026-01-01T00:00:00Z --to 2026-02-01T00:00:00Z \
  --max-parallel 4
```

## Throttling

Backfills share the coordinator with live runs. Cap their worker share with
`runtime.backfill_worker_share` (default `0.5`).

## Idempotency

Backfills write to a shadow partition and swap it in when the range completes,
so a failed backfill never leaves partial data behind.
