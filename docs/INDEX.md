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
| [Core Concepts](docs/getting-started/concepts.md) | docs-team | stable |
| [Install Quarry](docs/getting-started/install.md) | platform-eng | stable |
| [Quickstart: Your First Pipeline](docs/getting-started/quickstart.md) | platform-eng | stable |

### Guides
| Page | Owner | Stability |
| --- | --- | --- |
| [Backfill Runs](docs/guides/backfills.md) | operations | beta |
| [Batch Ingestion](docs/guides/batch-ingest.md) | data-platform | stable |
| [Schema Registry Setup](docs/guides/schema-registry.md) | data-platform | stable |
| [Streaming Ingestion](docs/guides/stream-ingest.md) | data-platform | beta |
| [Transforms and Enrichment](docs/guides/transforms.md) | analytics-eng | beta |

### Operations
| Page | Owner | Stability |
| --- | --- | --- |
| [Cluster Upgrades](docs/operations/upgrades.md) | sre | beta |
| [Monitoring Pipelines](docs/operations/monitoring.md) | sre | stable |
| [Retention and Archival](docs/operations/retention.md) | sre | stable |
| [Troubleshooting Guide](docs/operations/troubleshooting.md) | sre | stable |

### Reference
| Page | Owner | Stability |
| --- | --- | --- |
| [CLI Reference](docs/reference/cli.md) | core-runtime | stable |
| [Configuration Reference](docs/reference/config.md) | core-runtime | stable |
| [Glossary](docs/reference/glossary.md) | docs-team | stable |
| [HTTP API Reference](docs/reference/api.md) | core-runtime | stable |
<!-- END CATALOG -->

## Curated Reading Order

The entries below reference pages by their stable documentation id, which does not
change when a page moves. Resolve them against the page tree of the branch you are
working on.

<!-- BEGIN PATHS -->
1. **Install** — `install`
2. **First pipeline** — `quickstart`
3. **Mental model** — `concepts`
4. **Streaming** — `stream-ingest`
5. **Day-two operations** — `monitoring`
6. **When things break** — `troubleshooting`
7. **Terminology** — `glossary`
<!-- END PATHS -->

## Maintaining this index

Both blocks are maintained by hand. When pages move, are added or are retired,
rebuild them from the page tree instead of patching individual rows. Pages that
are not `published` (drafts, archived material) and files without front matter
(style notes) never appear in the catalogue.

Questions about the documentation set go to #quarry-docs.
