---
id: "upgrades"
title: "Cluster Upgrades"
owner: "sre"
section: "Operations"
status: "published"
stability: "beta"
---

# Cluster Upgrades

Quarry supports one minor version of skew between coordinator and agents.

## Rolling upgrade

1. Drain the coordinator: `quarry coordinator drain`.
2. Upgrade one agent and confirm it rejoins.
3. Upgrade the remaining agents in batches of 25%.
4. Upgrade the coordinator last.

## Rollback

Keep the previous image tag for seven days. A rollback requires stopping live
runs; checkpoints written by a newer minor version are not readable by an older
coordinator.
