# Schemas

This directory contains YAML-based schema files that define HICEL primitives and document kinds.

## Layout

- `schemas/primitives/` holds one schema per primitive.
- `schemas/documents/` holds one schema per document kind.
- `schemas/shared/` contains shared schema fragments (e.g., metadata).
- `schemas/compat/` stores HIPF compatibility references and HIPF profile schemas (`compat/hipf/`).

## Notes

- Schemas enforce required fields (`type`, `label`, `timestamp`, `metadata`) and UUID-only identifiers.
- Extension fields must use the `x-` prefix.
- Documentation for each schema is available under `docs/schemas/`.
