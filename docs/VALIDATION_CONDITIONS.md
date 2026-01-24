# Validation Conditions

HICEL validation combines structural checks (schema-level) with limited semantic assertions (rule-level). Use this list as the authoritative validation checklist.

## Structural schema checks

- Required fields exist: `type`, `label`, `timestamp`, `metadata`.
- `type` matches the schema-specific constant.
- `metadata` contains `uuid`, `source`, `status`, and `refs`.
- `metadata.uuid`, `id`, and `refs` values are UUIDs.
- Extension fields use the `x-` prefix.

## Document-kind checks

- `CorpusDocument` includes `header`, `scope`, and `entries`.
- `TimelineEntryDocument` includes `header` and `entry`.
- `WorldConstraintDocument` includes `header` and `constraints`.
- `SpecificationDocument` includes `header` and `sections`.
- `ModelDocument` includes `header` and `models`.
- `DatasetRecord` includes `header` and `records`.
- `EvaluationReport` includes `header` and `evaluation`.

## HIPF compatibility checks

- HIPF evaluation can operate using HICEL objects without schema extension.
- Field mappings match the canonical compatibility table in `docs/schemas/compat/hipf-mapping.md`.
- HICEL schemas retain HIPF-aligned `type`/`kind` constants.

## Semantic constraint checks

HICEL is valid only if the following constraints hold:

- No world semantics embedded in primitives.
- No cosmological or metaphysical assumptions exist in primitives.
- No genre constraints exist in primitives.
- No simulation requirement exists in primitives.

### Forbidden fields (must not appear)

Use this list as the minimum prohibited field set when validating semantic neutrality:

- `world`, `worldview`, `cosmology`, `pantheon`, `metaphysics`
- `genre`, `myth`, `magic`, `fate`, `destiny`
- `simulation`, `simulator`, `engine`, `runtime`
- `canon`, `lore`, `narrative_authority`

### Remediation guidance

Validation output must include remediation hints. Example: "Remove forbidden field `cosmology` from primitive data or move it to world-layer documents." 
