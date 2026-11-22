---
id: "troubleshooting"
title: "Troubleshooting Guide"
owner: "sre"
section: "Operations"
status: "published"
stability: "stable"
---

# Troubleshooting Guide

## Coordinator will not start

Check `quarry doctor --config ./quarry.yaml`. The most common cause is an expired
object-store credential.

## Tasks stay in PENDING

Agents register with the coordinator over gRPC on port 9110. Confirm the agents
can reach the coordinator address advertised in `coordinator.advertise_addr`.

## Sink commit timeouts

Raise `sink.commit_timeout` above the p99 of the target system, then restart the
coordinator. Checkpoints older than the sink's transaction timeout are rejected.
