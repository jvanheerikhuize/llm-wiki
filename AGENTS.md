# Agent Instructions for llm-wiki

This repository is maintained with the help of AI coding agents (Claude, Antigravity, Cursor, etc.).

## Overview
Persistent file-based LLM Wiki knowledge base for AI-assisted software delivery and knowledge synthesis.

## Key Rules
1. **Specifications & Epistemic Grounds:** Read compiled specifications in [`specs/README.md`](specs/README.md) (`specs/SPC-*.md`). Edit atomic epistemic records in `.specs/records/` and re-render via `python3 ~/.agents/skills/asdlc-spec-workflow/scripts/sync_specs.py --apply`.
2. **Design System:** Follow `Design-System: asdlc-meta-designsystem@latest` declared in [`TECH_STACK.md`](TECH_STACK.md).
3. **Knowledge Base Contract:** Read [`knowledge/AGENTS.md`](knowledge/AGENTS.md) before modifying `knowledge/`. Use `[[topic]]` wikilink cross-referencing and run `python3 knowledge/tools/kb.py lint --strict`.
4. **Workspace Coexistence:** Follow multi-agent rules in [`/home/jerry/Repos/AGENTS.md`](../AGENTS.md).
