---
id: REQ-0005
title: Interactive 2D and 3D knowledge graph visualization and static site publishing
status: active
because: [FCT-0004]
---

## Statement
The visualization generator MUST emit a static documentation configuration, a tag index, a connections table, and an interactive 2D and 3D knowledge graph colored by confidence band, published as the primary static site with the specification dashboard mounted at `/specs/`.

## Acceptance
- Given a valid wiki corpus
- When the visualization generator runs
- Then the homepage graph, connections table, status stylesheet, and static site configuration are generated without broken links
