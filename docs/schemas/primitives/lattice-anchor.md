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
- `pitfalls` (list of `{key, label, description?}`) — typical analytical pitfalls: reasoning errors a
  claim commits when it ignores the lattice (not systemic outcomes of the governed domain)

`key` values are local keys (`^[a-z0-9][a-z0-9_-]*$`), unique within the lattice; they are not
global identifiers.

## Profiles

- HIPF: `schemas/compat/hipf/channel-scan-lattice.yaml` requires `lattice_kind: channel_scan`,
  at least one trigger tag and one channel, and a `pitfalls` list.

## Lattice kinds

"Lattice" is used in the HIPF sense, not the order-theory sense (a partially ordered set with
joins and meets). HIPF uses the term for two distinct constructs:

| Kind | HIPF source | Organized by | Content | Role |
| --- | --- | --- | --- | --- |
| Channel-scan lattice (`channel_scan`) | `validators/CONSEQUENCE_LATTICES.md` | Shock type | Triggers, channels, typical pitfalls | Soft validation: prevents omitted second-order effects |
| Stateful consequence lattice | `validators/CONSEQUENCE_LATTICE_FRAMEWORK.md`, `lattices/examples/` | Systemic domain | Scope, triggers, ordinal state levels, propagation rules, failure modes | Gates plausibility (saturation testing) |

Only channel-scan lattices are encoded. Stateful lattices (state levels, propagation rules,
saturation) are not yet representable; the `consequence` kind is reserved for them.

## References

- Schema: `schemas/primitives/lattice-anchor.yaml`
