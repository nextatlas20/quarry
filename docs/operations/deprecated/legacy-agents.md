---
id: "legacy-agents"
title: "Legacy Agent Mode"
owner: "sre"
section: "Operations"
status: "archived"
stability: "experimental"
---

# Legacy Agent Mode

Legacy agent mode started tasks from a shared filesystem queue instead of the
coordinator RPC.

It was removed in 4.0. The page is kept for readers upgrading from 3.x.

## Migration notes

- Replace `agent.queue_dir` with `coordinator.advertise_addr`.
- Remove the cron entry that started `quarry-agent --legacy`.
- Legacy checkpoints are imported once by `quarry migrate --legacy-checkpoints`.
