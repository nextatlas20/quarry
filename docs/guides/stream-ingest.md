---
id: "stream-ingest"
title: "Streaming Ingestion"
owner: "data-platform"
section: "Guides"
status: "published"
stability: "beta"
---

# Streaming Ingestion

Streaming sources keep a consumer group per pipeline.

```yaml
source:
  kind: kafka
  brokers: [broker-a:9092, broker-b:9092]
  topic: events.raw
  group: quarry-events-to-parquet
```

## Checkpoint interval

The coordinator commits offsets only after the sink acknowledges a batch. The
default interval is 30 seconds; lower it for dashboards that need fresher data.

```yaml
runtime:
  checkpoint_interval: 10s
```

Streaming runs do not stop on their own. Use `quarry stop` or the HTTP API to
drain a run cleanly.
