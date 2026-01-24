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
- `schemas/` — machine-readable schema artifacts (placeholders in this starter repo)
- `templates/` — authoring templates (Markdown/YAML frontmatter patterns)
- `conventions/` — cross-cutting conventions
- `glossary/` — definitions and controlled vocabulary (non-world-specific)

## Status

Starter skeleton generated from an extraction of conventions observed in a HIPF-following corpus. Adjust as your conventions stabilize.
