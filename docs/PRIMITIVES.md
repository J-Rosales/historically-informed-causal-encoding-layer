# Candidate Schema Primitives

These are content-agnostic building blocks intended to be reused across world corpora.

## Primitives

- `DocumentHeader` (title, identifiers, classification, scope, refs)
- `ReferenceNode` (canonical id, aliases, external authority links)
- `EntityModel` (actor or institutional entity descriptor)
- `InstitutionModel` (roles, capacities, governance modes)
- `BeliefRegimeModel` (motifs, practices, transmission, authority)
- `CultureModel` (descriptive profile without ontology)
- `RegionAbstraction` (place/zone without geography)
- `TemporalMarker` (approximate date, range, uncertainty)
- `TimelineEntry` (minimal event/process pointer with refs)
- `PeriodizationIndex` (major/minor period sets)
- `StateSlice` (snapshot across domains)
- `ChangeEntry` (event/process/structural transformation/condition/crisis)
- `DeltaEncoding` (state change with causality links)
- `ConstraintProfile` (bounds and affordances)
- `CapabilityEnvelope` (capacity limits by domain)
- `ResourceEnvelope` (inputs/outputs and constraints)
- `PressureObject` (stressors/shocks)
- `ConditionObject` (derived persistent constraints)
- `CrisisObject` (derived multi-domain strain)
- `LatticeAnchor` (gating structures without enumerating world values)
- `LensModifier` (interpretive modifier without gating)
- `EvaluationContext` (inputs used by HIPF evaluators)
- `DomainBinding` (cross-domain references and link rules)
