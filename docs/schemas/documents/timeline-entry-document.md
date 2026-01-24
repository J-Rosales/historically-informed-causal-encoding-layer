# TimelineEntryDocument

## Purpose

Defines the document-kind container for `TimelineEntryDocument`. It composes primitives while preserving HICEL constraints.

## Required fields

- `type`
- `label`
- `timestamp`
- `metadata`
- `header`
- `entry`


## Optional fields

- `id` (UUID)
- `refs` (UUID list)
- `attributes` (open object for structured detail)
- `x-*` extension fields

## References

- Schema: `schemas/documents/timeline-entry-document.yaml`
