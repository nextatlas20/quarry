---
id: "plugin-sdk"
title: "Plugin SDK (Draft)"
owner: "core-runtime"
section: "Reference"
status: "draft"
stability: "experimental"
---

# Plugin SDK (Draft)

Plugins extend Quarry with custom sources, transforms and sinks.

## Entry points

```python
from quarry.plugin import hookimpl

@hookimpl
def register_transforms(registry):
    registry.add("scrub", ScrubTransform)
```

The SDK is unstable before 4.3. Pin the Quarry version in `pyproject.toml` and
expect breaking changes between minors.
