# SpecificationDocument

## Purpose

Defines the document-kind container for `SpecificationDocument`. It composes primitives while preserving HICEL constraints.

## Required fields

- `type`
- `label`
- `timestamp`
- `metadata`
- `header`
- `sections`


## Optional fields

- `id` (UUID)
- `refs` (UUID list)
- `attributes` (open object for structured detail)
- `x-*` extension fields

## References

- Schema: `schemas/documents/specification-document.yaml`
