---
id: "transforms"
title: "Transforms and Enrichment"
owner: "analytics-eng"
section: "Guides"
status: "published"
stability: "beta"
---

# Transforms and Enrichment

Transforms are declared as an ordered list and run in that order.

## SQL projection

```yaml
transforms:
  - kind: sql
    query: >
      select event_id, user_id, lower(event_name) as event_name
      from input
      where event_time > now() - interval '1' day
```

## Enrichment joins

```yaml
  - kind: lookup
    table: s3://reference/users/
    on: user_id
    columns: [plan_tier, country]
```

Joins are broadcast when the reference table is below 256 MB and shuffled above
that threshold.
