---
id: REQ-0002
title: Pluggable source ingestion with immutable raw artifacts and duplicate detection
status: active
because: [FCT-0002]
---

## Statement
The ingestion pipeline MUST copy incoming documents into an immutable raw archive, extract text through a prioritized adapter interface, record a content digest on the resulting source page, and warn on near-duplicate sources.

## Acceptance
- Given a new document placed in the ingestion inbox
- When the ingestion operation runs
- Then the raw artifact is archived immutably, a source page is stamped with its digest, and the inbox is cleared
