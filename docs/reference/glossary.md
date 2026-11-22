---
id: "glossary"
title: "Glossary"
owner: "docs-team"
section: "Reference"
status: "published"
stability: "stable"
---

# Glossary

**Agent** — worker process that executes tasks for a coordinator.

**Batch** — a bounded collection of records passed between operators.

**Checkpoint** — durable record of committed input offsets and sink state.

**Coordinator** — process that plans work, tracks checkpoints and serves the API.

**Pipeline** — the document that binds a source, transforms and a sink.

**Run** — one coordinator attempt over a bounded input range.

**Task** — the unit of work an agent executes for a run.
