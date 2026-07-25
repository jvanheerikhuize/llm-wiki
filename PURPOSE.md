# Purpose

**Problem:** AI-assisted software delivery (ASDLC framework) requires a knowledge base of patterns, decision trees, and domain-specific terminology, but no system exists to maintain it as a living document with search and wikilink traversal.

**Audience:** Framework users, Claude Code agents, and teams implementing ASDLC processes who need authoritative reference material on framework concepts.

**Key constraints:** Must be searchable (BM25 ranking), support wikilinks for navigation, auto-generate from a canonical source (no manual sync), and maintain backward compatibility as the framework evolves.

**Success metric:** A user or agent can search for an ASDLC concept (e.g., "gate taxonomy"), find authoritative documentation with embedded examples, and follow links to related concepts without hunting through scattered docs.
