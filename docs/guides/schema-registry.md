---
id: "schema-registry"
title: "Schema Registry Setup"
owner: "data-platform"
section: "Guides"
status: "published"
stability: "stable"
---

# Schema Registry Setup

Register the writer schema before the first pipeline run.

```bash
quarry schema register --subject events-value --file schema/events.avsc
```

## Compatibility modes

| Mode | Allowed change |
| --- | --- |
| BACKWARD | add optional fields, remove optional fields |
| FORWARD | add required fields with defaults |
| FULL | both of the above |

Set the mode per subject:

```bash
quarry schema mode --subject events-value --mode FULL
```

Readers resolve the writer schema by subject and version, so a pipeline never
needs the physical schema of the input files.
