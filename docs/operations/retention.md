---
id: "retention"
title: "Retention and Archival"
owner: "sre"
section: "Operations"
status: "published"
stability: "stable"
---

# Retention and Archival

Retention is expressed per dataset:

```yaml
retention:
  hot_days: 30
  cold_days: 730
  cold_store: s3://archive/orders/
```

The maintenance job runs at 02:00 UTC. It moves partitions older than
`hot_days` to the cold store and drops anything beyond `cold_days`.

## Restoring from the cold store

Cold partitions are registered in the metastore with a `cold:` prefix, so a
query can read them transparently if the coordinator has archive credentials.
