# Conventions

This file records cross-cutting conventions that HICEL-compliant corpora should follow.

## Frontmatter

- Use YAML frontmatter for all authored Markdown documents.
- Every document must declare:
  - `title`
  - `kind` (or `document_type`)
  - `status` (draft/active/deprecated)
  - `scope` (what it applies to)
  - `refs` (including HIPF anchors where relevant)

## Layer separation

- Keep diegetic narrative content separate from analytical constraints and modeling.
- Do not embed constraint definitions inside narrative documents.

## Neutral timeline summaries

- Timeline entries must remain minimal and non-resolving.
- Prefer fuzzy dating to false precision; encode uncertainty explicitly.

## References

- Prefer stable IDs.
- References must be resolvable within the corpus where possible.
- External authorities (including HIPF) must be listed under `refs`.
