# Repository Structure

Recommended layout for this repository:

```
historically-informed-causal-encoding-layer/
  docs/
    SCOPE_BOUNDARY.md
    EXTRACTED_PATTERNS.md
    PRIMITIVES.md
    SCHEMA_LAYERS.md
    ARCHITECTURE_MODEL.md
    REPO_STRUCTURE.md
    INTEROPERABILITY_RULES.md
    VALIDATION_CONDITIONS.md
    schemas/
      README.md
      primitives/
      documents/
      compat/
  schemas/
    README.md
    primitives/
    documents/
    shared/
    compat/
      hipf/
  templates/
    README.md
    DOCUMENT_HEADER_TEMPLATE.md
    TIMELINE_ENTRY_TEMPLATE.md
    CORPUS_DOCUMENT_TEMPLATE.md
    WORLD_CONSTRAINT_TEMPLATE.md
  conventions/
    conventions.md
  glossary/
    glossary.md
  LICENSE
  README.md
```

Notes:
- `schemas/` holds machine-readable schemas for primitives and document kinds.
- `schemas/compat/hipf/` holds HIPF profile schemas (primitive + HIPF vocabulary via `allOf`).
- `docs/schemas/` provides schema-specific guidance and HIPF compatibility notes.
- `templates/` provides authoring patterns intended to produce schema-valid documents.
