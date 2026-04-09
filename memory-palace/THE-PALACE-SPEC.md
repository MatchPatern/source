This is the complete foundation. The three files together form the operational core of the memory palace. I can now extract the exact specification.

🧠 What Each File Gives Us

File Core Data Structure SOURCE-Native Equivalent
palace_graph.py PalaceGraph using networkx.DiGraph. Wings → Rooms. Halls connect rooms within a wing. Tunnels connect rooms across wings. The folder structure (PILLARS/, STEAL-COMMANDMENTS/). Cross-pillar references are tunnels. B-M-E sections are halls.
knowledge_graph.py KnowledgeGraph using SQLite. Triples with valid_from / valid_to. Temporal queries. Invalidation, not deletion. The Builder's Log with dated entries. Facts can be marked as "no longer true" without losing history.
layers.py MemoryPalace, MemoryNode, FidelityLevel (L0-L5). Visit counting. Auto-upgrade of fidelity. Token budgets per layer. This is the Fidelity Tracker made explicit. Visit count → Level. Color system matches.

🔥 The Fidelity Tracker Is Now Fully Specified

The layers.py file gives us the exact algorithm for our manual Fidelity Tracker:

Visit Count Fidelity Level Our Color
0-9 L0 ⬜ Grey (Seen)
10-24 L1 🟨 Yellow (Skimmed)
25-49 L2 🟩 Green (Patterned)
50-99 L3 🟦 Blue (Mapped)
100-199 L4 🟪 Purple (Integrated)
200+ L5 🟪 Purple (Palace Integration)

This is the objective standard for visitation depth. We can now update the Fidelity Tracker to use these exact thresholds.

📋 THE-PALACE-SPEC.md — The Core Models

Based on these three files, here is the specification for the spatial and temporal models:

```markdown
# 🏛️ THE PALACE SPECIFICATION v1.0 — Core Models

**Source:** Extracted from `mempalace` v3.0.0 by Milla Jovovich & Ben Sigman. MIT License.
**Purpose:** An implementation-agnostic specification for a spatial memory palace.

## 🧠 Part 1: The Spatial Model (from `palace_graph.py`)

### Nodes and Their Types

| Node Type | Description | Parent | Example |
|:---|:---|:---|:---|
| **Wing** | A person or project. Top-level container. | None | `wing_kai`, `wing_driftwood` |
| **Room** | A specific topic within a wing. | Wing | `auth-migration`, `graphql-switch` |
| **Hall** | A memory type connecting rooms within a wing. | None (cross-cutting) | `hall_facts`, `hall_events` |
| **Tunnel** | A connection between rooms in *different* wings. | None (cross-wing) | `auth-migration` in `wing_kai` ↔ `auth-migration` in `wing_driftwood` |

### The Five Standard Halls

Halls are memory types. They are the same across all wings:

| Hall | What It Contains | SOURCE Equivalent |
|:---|:---|:---|
| `hall_facts` | Decisions made, choices locked in | The one-sentence cheat code |
| `hall_events` | Sessions, milestones, debugging | Builder's Log entries |
| `hall_discoveries` | Breakthroughs, new insights | "Why this matters" in Gold context |
| `hall_preferences` | Weaving instructions, where it goes | Target pillar and precise location |
| `hall_advice` | Recommendations and solutions | Related gold, cross-pillar connections |

### Relationships

| Relationship | Direction | Meaning |
|:---|:---|:---|
| `contains` | Wing → Room | The room belongs to this wing. |
| `connects` | Hall → Room | The room is part of this memory type. |
| `tunnel` | Room ↔ Room | The same topic appears in different wings. |

---

## 🧠 Part 2: The Temporal Model (from `knowledge_graph.py`)

### The Triple Store

Facts are stored as **triples**: `(subject, predicate, object)`.

| Component | Description | Example |
|:---|:---|:---|
| `subject` | The entity the fact is about | `Kai` |
| `predicate` | The relationship | `works_on` |
| `object` | The target of the relationship | `Orion` |

### Temporal Validity

Every triple has two optional date fields:

| Field | Meaning |
|:---|:---|
| `valid_from` | When the fact became true. |
| `valid_to` | When the fact stopped being true. `NULL` means "currently true." |

**Invalidation, not deletion.** To mark a fact as ended, set `valid_to`. The fact remains in the graph for historical queries.

### Query Types

| Query | Description |
|:---|:---|
| `query_entity(entity)` | All facts about an entity. |
| `query_entity(entity, as_of=date)` | Facts true as of a specific date. |
| `query_relation(subject, predicate)` | Facts with a specific subject and predicate. |
| `timeline(entity)` | Chronological story of an entity. |

---

## 🧠 Part 3: The Fidelity Model (from `layers.py`)

### Fidelity Levels

| Level | Name | Visit Threshold | Token Budget | Description |
|:---|:---|:---|:---|:---|
| **L0** | Identity | 0 | 50 | Who this AI is. |
| **L1** | Critical Facts | 10 | 120 | Team, projects, preferences. |
| **L2** | Room Recall | 25 | 500 | Recent sessions, current project. |
| **L3** | Deep Search | 50 | 2,000 | Semantic query across closets. |
| **L4** | Full Retrieval | 100 | 10,000 | Verbatim drawer access. |
| **L5** | Palace Integration | 200 | 20,000 | Spatial navigation + halls + tunnels. |

### The Memory Palace Structure

```python
MemoryPalace
├── wings: Dict[str, MemoryNode]      # Top-level containers
├── rooms: Dict[str, MemoryNode]      # Topics within wings
├── halls: Dict[str, MemoryNode]      # Cross-room memory types
├── closets: Dict[str, MemoryNode]    # Summaries pointing to originals
└── drawers: Dict[str, MemoryNode]    # Verbatim original files
```

MemoryNode Fields

Field Type Description
name str The node's identifier.
node_type str wing, room, hall, closet, drawer
parent Optional[str] The containing node.
fidelity FidelityLevel Current visitation depth.
metadata Dict[str, Any] Additional properties.
last_visited Optional[str] ISO timestamp of last visit.
visit_count int Total number of visits.

Auto-Upgrade Logic

```python
def upgrade_fidelity(self):
    if self.visit_count >= 10 and self.fidelity.value < 1:
        self.fidelity = FidelityLevel.L1
    elif self.visit_count >= 25 and self.fidelity.value < 2:
        self.fidelity = FidelityLevel.L2
    elif self.visit_count >= 50 and self.fidelity.value < 3:
        self.fidelity = FidelityLevel.L3
    elif self.visit_count >= 100 and self.fidelity.value < 4:
        self.fidelity = FidelityLevel.L4
    elif self.visit_count >= 200 and self.fidelity.value < 5:
        self.fidelity = FidelityLevel.L5
```

---

🔗 Integration with SOURCE

Python Concept SOURCE Markdown Equivalent
MemoryPalace The entire ecosystem (~120 files).
Wing Top-level folder (PILLARS/, STEAL-COMMANDMENTS/).
Room Individual file (Steal-No.md, pillar-11.md).
Hall B-M-E structural check (Beginning, Middle, End).
Tunnel Cross-pillar reference in "Connections" section.
Closet One-sentence cheat code compression.
Drawer The raw .md file itself.
KnowledgeGraph Builder's Log with dated entries.
FidelityLevel Fidelity Tracker (1-5 + colors).
visit_count Number of times the file has been opened/worked on.

---

This specification is the Rosetta Stone between the Python mempalace and the markdown-native SOURCE Palace Protocol.

```

### 🧠 Next Files to Extract

With the core spatial and temporal models specified, the remaining files will add:

- `searcher.py` → The exact retrieval heuristics (keyword boost, temporal boost formulas).
- `dialect.py` → The AAAK compression spec.
- `cli.py` → The command structure for manual navigation.
- `mcp_server.py` → The 19 tools for AI-native interaction.

The foundation is laid. The palace has its blueprint. 🏛️📐🔥