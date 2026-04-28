# The Elephant Observatory — Knowledge Graph

> *A 21st Century Orbis Pictus*

This repository is a complete, nightly export of the knowledge graph from
[The Elephant Observatory](https://theelephantobservatory.org) — a living map
of metamodernism, sensemaking, the metacrisis, game theory, consciousness studies,
and adjacent ideas.

Last synced: **2026-04-28** · 1000 nodes · 96 observers

---

## What is TEO?

The Elephant Observatory is an annotated, interconnected knowledge graph of the
ideas shaping civilisational sensemaking. Each node distils a concept from a
lecture, paper, or conversation; edges encode the relationships between them.

The platform is built for studying, not skimming. Nodes have three levels of
description — Apprentice, Adept, Magus — calibrated to how familiar you already
are with the ideas.

---

## Repository Structure

```
nodes/           one .md file per published knowledge node (named by slug)
observers/       one .md file per observer whose ideas are mapped
glossary.json    definitions for key terms in the knowledge domain
edges.json       all connections between nodes, with relationship types
LICENSE          CC-BY-NC-SA 4.0
README.md        this file
```

---

## Node Format

Each file in `nodes/` uses YAML frontmatter followed by Markdown content:

```yaml
---
slug: the-metacrisis
title: "The Metacrisis"
subtitle: "Existential risk as a generator function"
observer: "Daniel Schmachtenberger"
observer_slug: daniel-schmachtenberger
source_title: "The Metacrisis — with Daniel Schmachtenberger"
source_url: "https://youtube.com/..."
source_author: "Daniel Schmachtenberger"
tags: [metacrisis, existential-risk, sensemaking, game-theory]
edges:
  - target: multipolar-traps
    type: relates_to
  - target: game-b-dynamics
    type: prerequisite
created_at: "2026-03-01"
---

# The Metacrisis

Existential risk as a generator function

---

{main summary paragraph(s)}

## Apprentice

Accessible introduction for newcomers to the ideas.

## Adept

Assumes familiarity with the domain.

## Magus

Assumes deep background knowledge — no hand-holding.
```

### Frontmatter Fields

| Field | Description |
|-------|-------------|
| `slug` | URL-safe identifier, unique per node |
| `title` | Node title |
| `subtitle` | Short evocative subtitle |
| `observer` | Name of the thinker this idea is attributed to |
| `observer_slug` | Slug for the observer's profile in `observers/` |
| `source_title` | Title of the source material (talk, paper, etc.) |
| `source_url` | URL to the original source |
| `source_author` | Author of the source (may differ from observer) |
| `tags` | Topical tags — see `glossary.json` for definitions |
| `edges` | Connections to other nodes (see Edge Types below) |
| `created_at` | Date the node was added to the Observatory |

---

## Observer Format

Each file in `observers/` describes a thinker whose ideas appear in the graph:

```yaml
---
name: "Daniel Schmachtenberger"
slug: daniel-schmachtenberger
website: "https://civilizationemerging.com"
wikipedia: "https://en.wikipedia.org/wiki/Daniel_Schmachtenberger"
youtube: "https://youtube.com/@DanielSchmachtenberger"
---

Bio text here.
```

---

## Edge Types

Edges encode the directed relationship from one node to another:

| Type | Meaning |
|------|---------|
| `relates_to` | Conceptual connection — both ideas are in conversation |
| `prerequisite` | Understanding the source node helps understand the target |
| `conflicts` | The two ideas are in tension or direct disagreement |

The full edge list is also available as `edges.json`:

```json
[
  { "source_slug": "metacrisis", "target_slug": "multipolar-traps", "relationship_type": "relates_to" }
]
```

---

## Tiered Descriptions

Every node has three levels of description, each calibrated to a different depth
of prior knowledge:

- **Apprentice** — Plain language, no assumed background. Good for first contact with an idea.
- **Adept** — Assumes familiarity with the general domain. Uses field-specific vocabulary.
- **Magus** — Assumes deep background. Focuses on nuance, edge cases, and synthesis.

---

## Usage

This dataset is suitable for:

- Building alternative interfaces or visualisations of the knowledge graph
- Academic research on metamodernism, sensemaking, or the metacrisis
- Training data for non-commercial AI projects (with attribution)
- Personal study and annotation

### Loading with Python

```python
import json, os, re

def load_nodes(folder="nodes"):
    nodes = []
    for fname in os.listdir(folder):
        if fname.endswith(".md"):
            with open(os.path.join(folder, fname)) as f:
                nodes.append(f.read())
    return nodes

with open("glossary.json") as f:
    glossary = json.load(f)

with open("edges.json") as f:
    edges = json.load(f)
```

---

## Attribution

The ideas in this graph belong to the thinkers who originated them. TEO distils
and maps them; it does not claim authorship of the underlying concepts. Each node
links to its primary source.

If you build on this dataset, please credit:
- **The Elephant Observatory** — https://theelephantobservatory.org
- The individual **observers** named in each node

---

## License

This knowledge graph is licensed under
[CC-BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

You are free to share and adapt it for **non-commercial purposes**, provided you
give appropriate credit and distribute any derivatives under the same license.

Commercial use requires written permission from The Elephant Observatory.

---

*Updated nightly from the live Observatory.*
