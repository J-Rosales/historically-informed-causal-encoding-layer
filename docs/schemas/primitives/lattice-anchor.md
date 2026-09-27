# LatticeAnchor

## Purpose

Defines the core structure for the `LatticeAnchor` primitive. Use it to describe neutral, non-world-specific structures aligned with HICEL constraints.

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
- `lattice_kind` (string) — classification of the lattice; vocabulary set by a compat profile
- `scope` (string) — domain the lattice governs and explicitly excludes
- `trigger_tags` (unique string list) — tags of change entries that engage the lattice
- `channels` (list of `{key, label, description?}`) — impact channels to scan
- `failure_modes` (list of `{key, label, description?}`) — typical failure modes

`key` values are local keys (`^[a-z0-9][a-z0-9_-]*$`), unique within the lattice; they are not
global identifiers.

## Profiles

- HIPF: `schemas/compat/hipf/consequence-lattice.yaml` requires `lattice_kind: consequence`,
  at least one trigger tag and one channel, and a `failure_modes` list.

## References

- Schema: `schemas/primitives/lattice-anchor.yaml`
