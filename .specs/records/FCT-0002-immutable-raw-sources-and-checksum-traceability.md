---
id: FCT-0002
title: Immutable raw source artifacts with cryptographic checksums preserve provenance
status: active
evidence: knowledge/tools/ingest_cmd.py copies inbox files into knowledge/raw/, computes SHA-256 checksums, and stamps wiki/sources/*.md pages.
---

Preserving original source documents without modification and linking each compiled source page via a cryptographic digest allows every synthesized wiki claim to be audited against its exact origin.
