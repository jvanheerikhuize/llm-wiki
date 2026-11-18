---
id: REQ-0001
title: Manifest-driven schema and template scaffolding
status: active
because: [FCT-0001]
---

## Statement
The knowledge base MUST generate its frontmatter validation schema and per-type page templates from a single declarative manifest and fail validation when committed artifacts drift from the manifest.

## Acceptance
- Given a declarative knowledge base manifest defining base fields and page types
- When the scaffolding command is executed
- Then the frontmatter validation schema and page templates are regenerated deterministically with zero drift
