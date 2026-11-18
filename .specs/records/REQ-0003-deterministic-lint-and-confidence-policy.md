---
id: REQ-0003
title: Deterministic linting for schema compliance, link integrity, and confidence caps
status: active
because: [FCT-0001, FCT-0003]
---

## Statement
The linting operation MUST validate every wiki page against the generated schema, reject broken wikilinks, flag orphan or stale pages, and enforce the maximum confidence cap on unsourced pages.

## Acceptance
- Given a corpus of wiki pages with frontmatter and wikilinks
- When the strict lint check runs
- Then any schema violation, broken wikilink, or confidence cap breach causes a non-zero exit status
