# ModelDocument

## Purpose

Defines the document-kind container for `ModelDocument`. It composes primitives while preserving HICEL constraints.

## Required fields

- `type`
- `label`
- `timestamp`
- `metadata`
- `header`
- `models`


## Optional fields

- `id` (UUID)
- `refs` (UUID list)
- `attributes` (open object for structured detail)
- `x-*` extension fields

## References

- Schema: `schemas/documents/model-document.yaml`
