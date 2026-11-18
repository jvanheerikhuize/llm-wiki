---
id: FCT-0001
title: A single declarative manifest prevents schema and template drift
status: active
evidence: knowledge/manifest.yaml and knowledge/tools/scaffold.py generate frontmatter.schema.json and _templates/*.md with zero drift verified by CI.
---

Generating validation schemas and page templates directly from one declarative manifest guarantees that page structure, required fields, and lint policies never diverge across tools.
