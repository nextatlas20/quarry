# Quarry Documentation

Quarry is a schema-aware ingestion toolkit for analytics teams. This page is the
entry point to the documentation set: the catalogue below lists every published
page, and the curated reading order at the bottom is the path we recommend to new
team members.

## Documentation Catalogue

<!-- BEGIN CATALOG -->
### Getting Started
| Page | Owner | Stability |
| --- | --- | --- |
| [Core Concepts](docs/start/core-concepts.md) | docs-team | stable |
| [Installing Quarry](docs/start/install.md) | platform-eng | stable |
| [Quickstart: Your First Pipeline](docs/start/quickstart.md) | platform-eng | stable |

### Guides
| Page | Owner | Stability |
| --- | --- | --- |
| [Backfill Runs](docs/guides/backfills.md) | operations | experimental |
| [Batch Ingestion](docs/guides/batch-ingestion.md) | data-platform | stable |
| [Record Deduplication](docs/guides/deduplication.md) | analytics-eng | beta |
| [Schema Evolution](docs/guides/schema-evolution.md) | data-platform | stable |
| [Schema Registry Setup](docs/guides/schema-registry.md) | data-platform | stable |
| [Streaming Ingestion](docs/guides/streaming-ingestion.md) | data-platform | beta |
| [Transforms and Enrichment](docs/guides/transforms.md) | analytics-eng | beta |

### Operations
| Page | Owner | Stability |
| --- | --- | --- |
| [Cluster Upgrades](docs/operations/upgrades.md) | sre | beta |
| [Incident Runbook](docs/operations/incident-runbook.md) | sre | stable |
| [Monitoring Pipelines](docs/operations/monitoring.md) | sre | stable |
| [Retention and Archival](docs/operations/retention.md) | sre | stable |

### Reference
| Page | Owner | Stability |
| --- | --- | --- |
| [CLI Reference](docs/reference/cli.md) | core-runtime | stable |
| [Configuration Reference](docs/reference/config.md) | core-runtime | stable |
| [HTTP API Reference](docs/reference/api.md) | core-runtime | stable |
<!-- END CATALOG -->

## Curated Reading Order

The entries below reference pages by their stable documentation id, which does not
change when a page moves. Resolve them against the page tree of the branch you are
working on.

<!-- BEGIN PATHS -->
1. **Install** — [Installing Quarry](docs/start/install.md)
2. **First pipeline** — [Quickstart: Your First Pipeline](docs/start/quickstart.md)
3. **Mental model** — [Core Concepts](docs/start/core-concepts.md)
4. **Streaming** — [Streaming Ingestion](docs/guides/streaming-ingestion.md)
5. **Day-two operations** — [Monitoring Pipelines](docs/operations/monitoring.md)
<!-- END PATHS -->

## Maintaining this index

Both blocks are maintained by hand. When pages move, are added or are retired,
rebuild them from the page tree instead of patching individual rows. Pages that
are not `published` (drafts, archived material) and files without front matter
(style notes) never appear in the catalogue.

Questions about the documentation set go to #quarry-docs.
