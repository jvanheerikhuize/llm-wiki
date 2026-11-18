---
id: REQ-0004
title: Ranked corpus search and source-bundled claim verification
status: active
because: [FCT-0002, FCT-0003, FCT-0004]
---

## Statement
The toolchain MUST provide ranked search across frontmatter and body text with contextual excerpts, and MUST assemble a target page alongside its cited raw sources for claim-by-claim verification.

## Acceptance
- Given a populated knowledge base corpus
- When a user or agent queries a term or requests verification for a page identifier
- Then ranked matching pages with excerpts or the complete source-backed verification bundle are returned
