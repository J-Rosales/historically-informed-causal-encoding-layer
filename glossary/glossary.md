# Glossary

This glossary defines non-world-specific terms used by HICEL.

- **Canonical ID**: A stable identifier used to reference a document/entity across the corpus.
- **DocumentHeader**: YAML frontmatter block containing document metadata and references.
- **ConstraintLayer**: Analytical documents defining constraints, envelopes, and evaluations.
- **ContentLayer**: Diegetic narrative documents and non-analytical creative prose.
- **TemporalMarker**: Representation of time with uncertainty (date/range/ordering).
- **ChangeEntry**: Event, process, or structural transformation that modifies constraints. Conditions and crises are derived entries encoded as `ConditionObject` / `CrisisObject`.
- **DeltaEncoding**: Formal representation of how a change entry modifies state.
- **Lattice**: HIPF term for a structure that constrains plausible outcomes; not the order-theory sense. HIPF has two kinds: channel-scan lattices (soft checklists of impact channels per shock type) and stateful consequence lattices (domain-bounded, with ordinal state levels). See `docs/schemas/primitives/lattice-anchor.md`.
- **Pitfall**: A typical reasoning error recorded on a channel-scan lattice (e.g., rivals treated as passive). Distinct from a stateful lattice's failure modes, which are systemic outcomes.
- **ChannelMark**: Recorded scan result for one lattice channel within an evaluation (mark, consequences, mitigations).
- **Profile schema**: A compat schema that applies an external framework's vocabulary to a neutral primitive via `allOf`.
- **StateSlice**: Computed snapshot of active constraints/capabilities for a given time+scope.
- **ExternalAuthorityRef**: A reference link to an external authority (e.g., HIPF section).
