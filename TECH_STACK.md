# LLM Wiki — Technology Stack Reference

This document lives **outside** the epistemic specification corpus (`.specs/records/`) so that all assumptions (`ASM`), facts (`FCT`), questions (`QST`), requirements (`REQ`), and specifications (`SPC`) remain 100% technology-stack-neutral.

Spec-Blueprint: asdlc-meta-specs@latest
Design-System: asdlc-meta-designsystem@latest

---

## Current Knowledge Base Stack

| Layer | Technology | Role |
| :--- | :--- | :--- |
| **CLI & Toolchain** | **Python 3.10+** + **`PyYAML`** + **`jsonschema`** (`knowledge/tools/kb.py`) | Zero-service command-line toolchain (`scaffold`, `new`, `ingest`, `search`, `index`, `lint`, `verify`, `viz`, `purge`). |
| **Manifest & Schema** | **`knowledge/manifest.yaml`** -> **`knowledge/_schema/frontmatter.schema.json`** | Single source of truth generating Draft 2020-12 JSON Schema and page templates (`knowledge/_templates/*.md`). |
| **Binary Ingestion Adapters** | **`plaintext`** (stdlib), **`markitdown`** (Microsoft MarkItDown), **`docling`** (IBM Docling) | Pluggable extraction pipeline (`knowledge/ingest/adapters/`) converting raw documents into SHA-256-linked `wiki/sources/*.md` pages. |
| **Static Site Visualization** | **`mkdocs-material`** + **`pymdown-extensions`** + **`mkdocs-redirects`** + **`3d-force-graph`** | Primary static knowledge graph and searchable wiki published to GitHub Pages root (`/`). |
| **Design System & Spec Dashboard** | **ASDLC Meta-DesignSystem** (`asdlc-meta-designsystem@latest`) + **ASDLC Meta-Specs** (`asdlc-meta-specs@latest`) | `<ui-stat-tile>` KPI strip, `<ui-chip>` 2D/3D graph view switcher and `<ui-badge>` in `knowledge/wiki/index.md`; `tokens.css` and `mkdocs-theme.css` site-wide, with `assets/theme-sync.js` mirroring the palette to `data-theme` + bolted-on specification dashboard at `/specs/`. |

---

## Directory Layout

- `.specs/records/` — Hidden atomic epistemic specification records (`ASM`, `FCT`, `QST`, `REQ`, `SPC`).
- `specs/` — Auto-generated agent-facing specifications (`specs/README.md`, `specs/SPC-0001.md`, `specs/SPC-0002.md`).
- `knowledge/manifest.yaml` — Declarative knowledge base schema, confidence policy, lint toggles, and adapter priority.
- `knowledge/tools/` — `kb.py` CLI and subcommands (`scaffold.py`, `new.py`, `ingest_cmd.py`, `search.py`, `lint.py`, `verify.py`, `viz.py`, `purge.py`, `mkdocs_hooks.py`).
- `knowledge/raw/` — Immutable ingested source artifacts.
- `knowledge/wiki/` — Interlinked wiki pages (`sources/`, `entities/`, `concepts/`, `index.md`, `tags.md`).
