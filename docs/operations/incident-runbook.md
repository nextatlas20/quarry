---
id: "incident-runbook"
title: "Incident Runbook"
owner: "sre"
section: "Operations"
status: "published"
stability: "stable"
---

# Incident Runbook

## Severity levels

| Level | Meaning | Response |
| --- | --- | --- |
| SEV1 | data loss or a stalled production run | page the on-call engineer immediately |
| SEV2 | degraded freshness, no data loss | respond within 30 minutes |
| SEV3 | single pipeline failing repeatedly | next business day |

## First five minutes

1. Announce the incident in `#quarry-incidents`.
2. Capture `quarry status --json` from the affected coordinator.
3. Decide whether to stop the run or let it drain.

Never restart a coordinator during a sink commit; wait for the checkpoint to
settle first.
