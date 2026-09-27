# EvaluationContext

## Purpose

Defines the core structure for the `EvaluationContext` primitive. Use it to describe neutral, non-world-specific structures aligned with HICEL constraints.

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
- `subject_refs` (UUID list) — objects under evaluation (e.g., `ChangeEntry` IDs)
- `verdict` (string) — qualitative outcome; vocabulary set by a compat profile
- `rationale` (string) — human-readable explanation of the verdict
- `lattice_scans` (list) — per-lattice channel scans:
  - `lattice_ref` (UUID), `flagged_failure_modes` (lattice failure-mode keys)
  - `channel_marks`: `{channel_key, mark, immediate?, delayed?, mitigations?}`
  - `mitigations`: `{description, refs?}` where `refs` point to the structural basis

No probability, score, or likelihood fields are defined. `EvaluationReport` carries these fields
through its `evaluation` property.

## Profiles

- HIPF: `schemas/compat/hipf/evaluation-context.yaml` requires `verdict` ∈ `plausible`,
  `conditionally_plausible`, `implausible`, at least one `subject_refs` entry, and channel
  `mark` ∈ `present`, `unknown`, `unknown_intentional_omission`, `not_applicable`.

## References

- Schema: `schemas/primitives/evaluation-context.yaml`
