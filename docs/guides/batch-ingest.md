---
id: "batch-ingest"
title: "Batch Ingestion"
owner: "data-platform"
section: "Guides"
status: "published"
stability: "stable"
---

# Batch Ingestion

Batch sources read whole files and split them into record batches.

```yaml
source:
  kind: files
  path: s3://landing/orders/
  format: parquet
  batch_records: 200000
```

## Partition discovery

Paths of the form `key=value/` are treated as partitions. Quarry infers the
partition column types from the first thousand files and fails fast on a
conflict.

## Recommended layout

Keep files between 128 MB and 1 GB. Smaller files increase coordinator overhead;
larger files delay checkpointing.
