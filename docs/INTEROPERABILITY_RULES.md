# Interoperability Rules

- HICEL consumes HIPF terminology by reference only; no HIPF modification.
- HICEL remains version-agnostic by isolating HIPF-dependent mappings in `schemas/compat/`.
- HICEL supports multiple world corpora by keeping all world content outside this repository.
- HICEL supports multiple cosmologies/metaphysics by prohibiting domain semantics in primitives.
- HICEL stays content-neutral by requiring `refs` for external authority and forbidding canonical enumerations.
- HICEL exposes deterministic schemas for tools (YAML/JSON) without enforcing narrative truth.
