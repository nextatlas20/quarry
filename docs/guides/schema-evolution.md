---
id: "schema-evolution"
title: "Schema Evolution"
owner: "data-platform"
section: "Guides"
status: "published"
stability: "stable"
---

# Schema Evolution

Quarry applies schema changes at write time, never at read time.

## Adding a column

Register the new schema with an optional field and restart the pipeline. Existing
partitions stay readable because the reader projects missing columns as null.

## Widening a type

`int` to `long` and `float` to `double` are safe widenings. Anything else
requires a new subject version and a backfill.

## Removing a column

Mark the field deprecated, wait for the retention window, then remove it in the
next major version.
