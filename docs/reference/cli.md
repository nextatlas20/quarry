---
id: "cli-ref"
title: "CLI Reference"
owner: "core-runtime"
section: "Reference"
status: "published"
stability: "stable"
---

# CLI Reference

`quarry` is a single binary with subcommands.

| Command | Purpose |
| --- | --- |
| `quarry run` | start a pipeline from a document |
| `quarry backfill` | replay a bounded historical range |
| `quarry status` | print run state, optionally as JSON |
| `quarry stop` | drain a running pipeline |
| `quarry doctor` | check configuration and connectivity |
| `quarry schema` | register schemas and set compatibility |

Every subcommand accepts `--config` and `--log-level`. `quarry run --once`
processes the available input and exits, which is useful in CI.
