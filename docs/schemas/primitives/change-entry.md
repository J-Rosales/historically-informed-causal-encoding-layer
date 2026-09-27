# ChangeEntry

## Purpose

Defines the core structure for the `ChangeEntry` primitive. Use it to describe neutral, non-world-specific structures aligned with HICEL constraints.

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
- `entry_kind` (string) — classification of the change; vocabulary set by a compat profile
- `temporal_ref` (UUID) — `TemporalMarker` binding the change in time
- `participant_refs` (UUID list) — entities/institutions participating in the change
- `affected_refs` (UUID list) — systems, constraints, or profiles whose state or rules the change alters
- `trigger_tags` (unique string list) — tags matched against lattice `trigger_tags`

## Profiles

- HIPF: `schemas/compat/hipf/change-entry.yaml` requires `entry_kind` ∈ `event`, `process`,
  `structural_transformation`. Conditions and crises use `ConditionObject` / `CrisisObject`.

## References

- Schema: `schemas/primitives/change-entry.yaml`
