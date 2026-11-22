---
id: "concepts"
title: "Core Concepts"
owner: "docs-team"
section: "Getting Started"
status: "published"
stability: "stable"
---

# Core Concepts

Quarry has four building blocks.

- **Source** — reads records from a filesystem, an object store or a message
  queue and emits record batches.
- **Transform** — maps one batch to another batch. Transforms are stateless
  unless they declare a window.
- **Sink** — writes batches to the target system and participates in the
  two-phase commit that makes a run exactly-once.
- **Checkpoint** — the durable record of what has been committed.

A *run* is one coordinator attempt over a bounded input range. An *agent* is the
worker process that executes tasks handed out by the coordinator.
