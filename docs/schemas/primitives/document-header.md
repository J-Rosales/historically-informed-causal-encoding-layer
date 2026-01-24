# DocumentHeader

## Purpose

Defines the core structure for the `DocumentHeader` primitive. Use it to describe neutral, non-world-specific structures aligned with HICEL constraints.

## Required fields

- `type`
- `label`
- `timestamp`
- `metadata`

## Optional fields

- `id` (UUID)
- `refs` (UUID list)
- `attributes` (open object for structured detail)
- `x-*` extension fields

## References

- Schema: `schemas/primitives/document-header.yaml`
