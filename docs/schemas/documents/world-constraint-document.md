# WorldConstraintDocument

## Purpose

Defines the document-kind container for `WorldConstraintDocument`. It composes primitives while preserving HICEL constraints.

## Required fields

- `type`
- `label`
- `timestamp`
- `metadata`
- `header`
- `constraints`


## Optional fields

- `id` (UUID)
- `refs` (UUID list)
- `attributes` (open object for structured detail)
- `x-*` extension fields

## References

- Schema: `schemas/documents/world-constraint-document.yaml`
