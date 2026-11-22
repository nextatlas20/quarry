---
id: "install"
title: "Installing Quarry"
owner: "platform-eng"
section: "Getting Started"
status: "published"
stability: "stable"
---

# Install Quarry

Quarry ships as a single Python package plus an optional native wheel for the
columnar reader.

## Requirements

- Python 3.10 or newer
- 4 GB of RAM for the coordinator process
- A reachable object store (S3, GCS, or a local filesystem path)

## Install from PyPI

```bash
python -m pip install "quarry-toolkit==4.2.*"
quarry --version
```

## Verify the installation

```bash
quarry doctor --config ./quarry.yaml
```

`quarry doctor` checks the parser, the object-store credentials and the schema
registry connection. It exits non-zero with a short diagnostic when a check
fails.
