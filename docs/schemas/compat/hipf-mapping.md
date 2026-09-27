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

## HIPF profile schemas

Primitives stay vocabulary-neutral; HIPF vocabularies live only in `schemas/compat/hipf/`.
Each profile is `allOf` the primitive plus HIPF value constraints.

| Profile | Primitive | HIPF source | Constrained values |
| --- | --- | --- | --- |
| `compat/hipf/change-entry.yaml` | `ChangeEntry` | `change_entries/HISTORICAL_CHANGE_ENTRY_FRAMEWORK.md` §II | `entry_kind`: `event`, `process`, `structural_transformation` |
| `compat/hipf/channel-scan-lattice.yaml` | `LatticeAnchor` | `validators/CONSEQUENCE_LATTICES.md` | `lattice_kind`: `channel_scan`; triggers, channels, pitfalls required |
| `compat/hipf/evaluation-context.yaml` | `EvaluationContext` | `evaluation/PLAUSIBILITY_EVALUATION_FRAMEWORK.md` §V; `validators/CONSEQUENCE_LATTICES.md` (Usage) | `verdict`: `plausible`, `conditionally_plausible`, `implausible`; `mark`: `present`, `unknown`, `unknown_intentional_omission`, `not_applicable` |

HIPF evaluates admissibility, not probability; no profile defines likelihood or score fields.

### Coverage

- Covered: entry typing (§II of the change-entry framework), channel scans, and verdicts (§V).
- Not covered: stateful consequence lattices and the stress and saturation steps that use them
  (`PLAUSIBILITY_EVALUATION_FRAMEWORK.md` §IV.3–IV.4). See `docs/schemas/primitives/lattice-anchor.md`.

## Constraints enforced in schema

- `type` is a constant per schema to enforce HIPF kind matching.
- `metadata.uuid` and `id` are UUID-only.
- `metadata` is required to enforce provenance, status, and references.
