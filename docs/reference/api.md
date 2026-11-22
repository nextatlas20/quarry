---
id: "api-ref"
title: "HTTP API Reference"
owner: "core-runtime"
section: "Reference"
status: "published"
stability: "stable"
---

# HTTP API Reference

The coordinator serves JSON over HTTP on `:9108`.

## Endpoints

| Method | Path | Purpose |
| --- | --- | --- |
| GET | `/v1/runs` | list runs and their state |
| GET | `/v1/runs/{id}` | run detail, counters and checkpoint id |
| POST | `/v1/runs` | start a run from a pipeline document |
| POST | `/v1/runs/{id}/stop` | drain and stop a run |
| GET | `/v1/health` | liveness and build version |

## Authentication

Send `Authorization: Bearer <token>` when `coordinator.auth_token` is set. The
API is read-only when the coordinator runs with `--read-only`.
