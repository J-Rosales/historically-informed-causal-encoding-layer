# Extracted Patterns

These patterns are generalized from a HIPF-following corpus and are intended as reusable conventions.

## Patterns

- **Document metadata in YAML frontmatter**
  - Consistent metadata blocks (e.g., `title`, `document_type`/`kind`, `scope`/`status`, `refs`) precede content.
  - **Candidate schema element:** `DocumentHeader` with `identifiers`, `classification`, `scope`, `refs`.

- **Diegetic vs non-diegetic separation by directory**
  - Narrative corpus is isolated from analytical constraints and belief modeling.
  - **Candidate schema element:** `ContentLayer` vs `ConstraintLayer` separation in repo and schema namespaces.

- **Thin chronology index with neutral summaries**
  - Timeline entries emphasize minimal, non-resolving summaries and fuzzy dating.
  - **Candidate schema element:** `TimelineEntry` with `date`, `status`, `scope`, `refs`, and minimal summary text.

- **Periodization split into major narrative index and minor structured subperiods**
  - Major periods are human-readable; minor periods are structured lists for indexing.
  - **Candidate schema element:** `PeriodizationIndex` with `MajorPeriods` (narrative) and `MinorPeriods` (structured list).

- **World constraints authored as instantiations, not frameworks**
  - Constraints assert parameterization without redefining global plausibility.
  - **Candidate schema element:** `WorldConstraint` with explicit HIPF anchors and non-authoritative status markers.

- **Explicit HIPF reference pointers**
  - World-instance documents carry explicit HIPF reference links.
  - **Candidate schema element:** `ExternalAuthorityRef` field in constraint-oriented schemas.
