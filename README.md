# Historically-Informed Causal Encoding Layer (HICEL)

HICEL is an intermediary implementation layer between HIPF (theory/validation) and world-specific corpora (instantiation).
It defines reusable **schemas, conventions, and encodings** for representing worlds as causal systems without embedding world-specific semantics.

## Layering

```
HIPF (theory/validation)
  ↓
HICEL (schemas/conventions/tools)
  ↓
World corpora (content/meaning/instantiation)
```

## Repository contents

- `docs/` — normative specifications and rationale
- `docs/schemas/` — schema-specific guidance and HIPF compatibility notes
- `schemas/` — machine-readable YAML schema artifacts for primitives and document kinds
- `templates/` — authoring templates (Markdown/YAML frontmatter patterns)
- `conventions/` — cross-cutting conventions
- `glossary/` — definitions and controlled vocabulary (non-world-specific)

## Status

Starter repository with initial schema coverage and validation guidance. Extend as conventions stabilize.
