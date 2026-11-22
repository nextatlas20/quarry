---
id: "quickstart"
title: "Quickstart: Your First Pipeline"
owner: "platform-eng"
section: "Getting Started"
status: "published"
stability: "stable"
---

# Quickstart: Your First Pipeline

A pipeline is a YAML document with a source, zero or more transforms and a sink.

```yaml
name: events-to-parquet
source:
  kind: files
  path: s3://demo-bucket/events/
transforms:
  - kind: cast
    column: event_time
    to: timestamp
sink:
  kind: parquet
  path: s3://demo-bucket/curated/events/
```

Run it once:

```bash
quarry run --pipeline events-to-parquet.yaml --once
```

The coordinator writes a checkpoint under `.quarry/checkpoints/` so a second run
resumes where the first stopped.
