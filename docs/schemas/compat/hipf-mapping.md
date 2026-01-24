# HIPF Compatibility Mapping

This mapping describes a strict field-by-field alignment between HICEL schema fields and HIPF expectations. It is documentation-only and serves as the authoritative compatibility reference.

## Core mapping

| HICEL field | HIPF field | Notes |
| --- | --- | --- |
| `type` | `kind` | Required for type alignment. |
| `label` | `title` | Human-readable label/title. |
| `timestamp` | `time` | ISO 8601 timestamp alignment. |
| `id` | `id` | UUID-only identifier in both layers. |
| `metadata.uuid` | `uuid` | Canonical UUID identity. |
| `metadata.source` | `source` | Provenance/ingest origin. |
| `metadata.status` | `status` | Draft/final/archived status. |
| `metadata.refs` | `refs` | UUID list for canonical references. |
| `refs` | `refs` | Cross-object linking. |
| `attributes` | `data` | Payload-like neutral data container. |

## Constraints enforced in schema

- `type` is a constant per schema to enforce HIPF kind matching.
- `metadata.uuid` and `id` are UUID-only.
- `metadata` is required to enforce provenance, status, and references.
