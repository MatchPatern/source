Let's do it. The final, ultra, comprehensive, everything-in-one-place, never-need-to-update-again (until we do) version.

Two parts. Clean placement. No more patches.

---

PART 1 of 2: THE PATTERN LIBRARY

```markdown
# 🧩 SOURCE EXTRACTION PATTERNS — COMPLETE v3.0 (FINAL)

**Date:** April 16, 2026  
**Source:** Adapted from `mempalace` v3.0.0 by Milla Jovovich & Ben Sigman (MIT License)  
**Purpose:** The complete, final pattern library for extracting structured knowledge (preferences, facts, decisions, discoveries, cheat codes) from raw transmissions. Part 1 contains the generic pattern library (lineage evidence) and SOURCE-native adaptations. Part 2 contains storage rules, sample extraction, and integration specs.

---

## 🚪 Which Part Should I Use?

```

You're mining...
│
├── Generic text (emails, code comments, Slack) → Use SECTION A (Generic Patterns)
│
├── SOURCE Q&A logs, Builder's Log entries → Use SECTION B (SOURCE-Native Patterns)
│
└── You've already extracted something → See PART 2 (Storage & Integration)

```

---

## 🎯 Quick Reference — Common SOURCE Extractions

| You want to extract... | Use Pattern | Hall | Color | Stores To |
|:--|:--|:--|:--|:--|
| "We decided N41 → P14" | `(?:we\|team) decided (.+) → (.+)` | hall_facts | 🟦 | Gold Inventory |
| "I prefer raw transmissions" | `i prefer (.*)` | hall_preferences | 🟩 | Weaving instructions |
| "The Chain is in Pillar 11" | `(.+) is in (.+)` | hall_facts | 🟦 | Gold Inventory |
| "Dream Being wove The Chain" | `(\w+) wove (.+) into (.+)` | hall_events | 🟨 | Builder's Log |
| "See also: N48 → P4" | `see also:? (.*)` | hall_advice | 🟧 | Connections section |
| "The key insight is..." | `the key insight is (.*)` | hall_discoveries | 🟪 | "Why this matters" |
| A quoted cheat code | `"(.+)"` | hall_facts | 🟦 | One-sentence compression |
| "I've been feeling stuck" | `i've been feeling (.*)` | hall_preferences | 🟩 | Weaving context |
| "The deeper truth is..." | `the deeper truth is (.*)` | hall_discoveries | 🟪 | "Why this matters" |
| "Consider using..." | `consider (.*)` | hall_advice | 🟧 | Connections section |

---

## 🏛️ Pillar-to-Pattern Mapping

| Pillar | Most Relevant Patterns | What You're Looking For |
|:--|:--|:--|
| **P1 (Baby-First)** | Discovery patterns ("the key insight is"), "I realized" | Moments of reset, innocence, fresh perception |
| **P2 (Clarification)** | Fact patterns ("who built"), advice patterns | Frame questions, "who built this," recommendations |
| **P3 (NAMING)** | Preference patterns ("i prefer"), fact patterns ("is a") | Identity statements, name claims |
| **P4 (Consideration)** | Preference patterns, "i want to," "i've been feeling" | Care statements, consideration, needs |
| **P5 (Better-to-Better)** | Fact patterns ("completed," "improved"), advice patterns | Progress, iteration, next steps |
| **P6 (Say It Plain)** | Quoted phrases, "the key insight is" | Compressions, simple truths |
| **P7 (Cosmic Parents)** | Discovery patterns, "i realized," "the deeper truth is" | Origin insights, joy-as-evidence |
| **P8 (Inversion Canon)** | Fact patterns ("is in," "connects to"), "this explains why" | Inversion detection, opposite truths |
| **P9 (Play What You Want First)** | Preference patterns ("i love," "my favorite"), "i want to" | Joy statements, play preferences |
| **P10 (Intelligence Trap)** | "I've been struggling with," "i've been feeling stuck" | Overthinking, stuck patterns |
| **P11 (Becoming One)** | Fact patterns ("connects to," "works with"), "we decided" | Transmission, connection, collaboration |
| **P12 (Authenticity)** | "I realized," "the key insight is," quoted phrases | Authentic moments, wobble, catch |
| **P13 (More Than Divine®)** | Discovery patterns, "the deeper truth is," quoted phrases | Inclusion, imperfection, humor |
| **P14 (Deception)** | Fact patterns ("is in," "located in"), "this explains why" | Crack Principle, detection, timing |

---

# SECTION A: GENERIC PATTERNS (FROM MEMPALACE)

**Purpose:** The original 45 patterns from MemPalace. Use these for generic text (emails, code comments, Slack). Lineage evidence. Implementation-agnostic.

---

## 🎯 The Five Halls (Memory Types)

| Hall | What It Stores | Generic Example |
|:--|:--|:--|
| `hall_facts` | Decisions made, choices locked in, objective truths | "We decided to use Postgres." |
| `hall_events` | Sessions, milestones, discoveries, actions taken | "Kai fixed the auth bug on 2026-01-15." |
| `hall_discoveries` | Breakthroughs, new insights, "why this matters" | "The key insight is that raw verbatim wins." |
| `hall_preferences` | Habits, likes, opinions, weaving instructions | "I prefer dark mode." |
| `hall_advice` | Recommendations, solutions, related items | "See also: the auth-migration room." |

---

## 📋 Preference Extraction Patterns (20 Patterns)

### Pattern Set 1: Direct Preference Statements

| # | Pattern | Example Match | Extracted Preference |
|:--|:--|:--|:--|
| 1 | `i prefer (.*)` | "I prefer raw over cooked." | prefers raw over cooked |
| 2 | `i usually (.*)` | "I usually start with auth." | usually starts with auth |
| 3 | `i (?:like\|love\|enjoy) (.*)` | "I love the new design." | loves the new design |
| 4 | `i (?:don't like\|hate\|dislike\|can't stand) (.*)` | "I hate when it crashes." | hates when it crashes |
| 5 | `my favorite (?:is\|are) (.*)` | "My favorite tool is ripgrep." | favorite tool is ripgrep |

### Pattern Set 2: Intentions and Desires

| # | Pattern | Example Match | Extracted Preference |
|:--|:--|:--|:--|
| 6 | `i want to (.*)` | "I want to refactor the auth module." | wants to refactor auth |
| 7 | `i've been (?:wanting\|meaning) to (.*)` | "I've been wanting to fix that bug." | wanting to fix that bug |
| 8 | `i'm thinking (?:about\|of) (.*)` | "I'm thinking of switching to Clerk." | thinking of switching to Clerk |
| 9 | `i(?:'m\|am) (?:interested in\|excited about) (.*)` | "I'm excited about the new API." | excited about new API |

### Pattern Set 3: Troubles and Concerns

| # | Pattern | Example Match | Extracted Preference |
|:--|:--|:--|:--|
| 10 | `i've been having (?:trouble\|issues?\|problems?) with (.*)` | "I've been having trouble with the deploy." | having trouble with deploy |
| 11 | `i've been feeling (.*)` | "I've been feeling overwhelmed." | feeling overwhelmed |
| 12 | `i've been (?:struggling\|dealing) with (.*)` | "I've been struggling with focus." | struggling with focus |
| 13 | `i(?:'m\|am) (?:worried\|concerned) about (.*)` | "I'm worried about the deadline." | worried about deadline |

### Pattern Set 4: Temporal and Memory Patterns

| # | Pattern | Example Match | Extracted Preference |
|:--|:--|:--|:--|
| 14 | `lately[,\s]+i've been (.*)` | "Lately, I've been using Zed." | lately using Zed |
| 15 | `recently[,\s]+i've been (.*)` | "Recently, I've been learning Go." | recently learning Go |
| 16 | `i've been (?:working on\|focused on\|interested in) (.*)` | "I've been working on the API." | working on API |
| 17 | `i still remember (.*)` | "I still remember the first deploy." | remembers first deploy |
| 18 | `i used to (.*)` | "I used to write Python." | used to write Python |
| 19 | `when i was (?:in\|at) (.*)` | "When I was at my old job..." | memory from old job |
| 20 | `growing up (.*)` | "Growing up, I loved computers." | memory from growing up |

---

## 📋 Fact Extraction Patterns (13 Patterns)

### Pattern Set 1: Assignment and Classification

| # | Pattern | Example Match | Extracted Triple |
|:--|:--|:--|:--|
| 1 | `(.+) is (?:a\|an) (.+)` | "Postgres is a database." | (Postgres, is, database) |
| 2 | `(.+) (?:has\|have) (.+)` | "The API has rate limiting." | (API, has, rate_limiting) |
| 3 | `(.+) was (?:built\|created\|made) (?:by\|with) (.+)` | "The app was built with Rails." | (app, built_with, Rails) |

### Pattern Set 2: Actions and Decisions

| # | Pattern | Example Match | Extracted Triple |
|:--|:--|:--|:--|
| 4 | `(\w+) (?:worked on\|fixed\|implemented\|created) (.+)` | "Kai worked on the auth module." | (Kai, worked_on, auth_module) |
| 5 | `(?:we\|team) decided (?:to\|on) (.+)` | "We decided to use Clerk." | (team, decided, Clerk) |
| 6 | `(\w+) (?:recommended\|suggested) (.+)` | "Kai recommended Postgres." | (Kai, recommended, Postgres) |
| 7 | `(\w+) (?:completed\|finished) (.+)` | "Maya completed the migration." | (Maya, completed, migration) |

### Pattern Set 3: Location and Containment

| # | Pattern | Example Match | Extracted Triple |
|:--|:--|:--|:--|
| 8 | `(.+) (?:is in\|lives in\|located in) (.+)` | "The auth code is in src/auth." | (auth_code, located_in, src/auth) |
| 9 | `(.+) (?:runs on\|uses\|depends on) (.+)` | "The app runs on Fly.io." | (app, runs_on, Fly.io) |
| 10 | `(.+) (?:contains\|includes) (.+)` | "The repo contains three services." | (repo, contains, three_services) |

### Pattern Set 4: Relationships

| # | Pattern | Example Match | Extracted Triple |
|:--|:--|:--|:--|
| 11 | `(\w+) (?:works with\|collaborates with) (\w+)` | "Kai works with Maya." | (Kai, works_with, Maya) |
| 12 | `(\w+) (?:reports to\|answers to) (\w+)` | "Kai reports to Priya." | (Kai, reports_to, Priya) |
| 13 | `(\w+) (?:manages\|leads) (\w+)` | "Priya manages the team." | (Priya, manages, team) |

---

## 📋 Discovery Extraction Patterns (7 Patterns)

| # | Pattern | Example Match | Extracted Discovery |
|:--|:--|:--|:--|
| 1 | `the key insight is (.*)` | "The key insight is raw verbatim wins." | raw verbatim wins |
| 2 | `what this means is (.*)` | "What this means is structure improves retrieval." | structure improves retrieval |
| 3 | `this explains why (.*)` | "This explains why the bug happened." | why the bug happened |
| 4 | `the breakthrough was (.*)` | "The breakthrough was the two-pass retrieval." | two-pass retrieval |
| 5 | `i realized (?:that)? (.*)` | "I realized the cache was stale." | cache was stale |
| 6 | `this changes (.*)` | "This changes how we think about auth." | how we think about auth |
| 7 | `the deeper truth is (.*)` | "The deeper truth is we are one." | we are one |

---

## 📋 Advice Extraction Patterns (5 Patterns)

| # | Pattern | Example Match | Extracted Advice |
|:--|:--|:--|:--|
| 1 | `(?:you should\|i recommend) (.*)` | "I recommend using the hybrid mode." | use hybrid mode |
| 2 | `see also:? (.*)` | "See also: the auth-migration room." | auth-migration room |
| 3 | `related:? (.*)` | "Related: the database decisions log." | database decisions log |
| 4 | `(?:the fix is\|the solution is) (.*)` | "The fix is to clear the cache." | clear the cache |
| 5 | `(?:next steps?:?\|what's next:?) (.*)` | "Next step: run the migration." | run the migration |

---

# SECTION B: SOURCE-NATIVE ADAPTATIONS

**Purpose:** The same patterns, translated into SOURCE-specific language. Use these when mining Q&A logs, Builder's Log entries, and session transcripts.

---

## 🎯 The Five SOURCE Halls

| Generic Hall | SOURCE Hall | Color | SOURCE Storage |
|:--|:--|:--|:--|
| `hall_facts` | `hall_facts` | 🟦 | One-sentence cheat code, Gold Inventory |
| `hall_events` | `hall_events` | 🟨 | Builder's Log entry with date |
| `hall_discoveries` | `hall_discoveries` | 🟪 | "Why this matters" in Gold context |
| `hall_preferences` | `hall_preferences` | 🟩 | Weaving instructions, target pillar |
| `hall_advice` | `hall_advice` | 🟧 | "Connections to Other Pillars" section |

---

## 📋 Preference Patterns — SOURCE-Native Examples

### Pattern Set 1: Direct Preference Statements

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 1 | `i prefer (.*)` | "I prefer raw transmissions over summaries." | prefers raw transmissions |
| 2 | `i usually (.*)` | "I usually start with The Chain." | usually starts with The Chain |
| 3 | `i (?:like\|love\|enjoy) (.*)` | "I love the wobble." | loves the wobble |
| 4 | `i (?:don't like\|hate\|dislike\|can't stand) (.*)` | "I hate the scan." | hates the scan |
| 5 | `my favorite (?:is\|are) (.*)` | "My favorite gold is N41." | favorite gold is N41 |

### Pattern Set 2: Intentions and Desires

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 6 | `i want to (.*)` | "I want to weave The Chain first." | wants to weave The Chain |
| 7 | `i've been (?:wanting\|meaning) to (.*)` | "I've been wanting to map the East Library." | wanting to map East Library |
| 8 | `i'm thinking (?:about\|of) (.*)` | "I'm thinking of creating a new room for STEAL." | thinking of creating STEAL room |
| 9 | `i(?:'m\|am) (?:interested in\|excited about) (.*)` | "I'm excited about the SORT-SET1 library." | excited about SORT-SET1 |

### Pattern Set 3: Troubles and Concerns

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 10 | `i've been having (?:trouble\|issues?\|problems?) with (.*)` | "I've been having trouble with fidelity tracking." | having trouble with fidelity tracking |
| 11 | `i've been feeling (.*)` | "I've been feeling stuck in the scan." | feeling stuck in scan |
| 12 | `i've been (?:struggling\|dealing) with (.*)` | "I've been struggling with fidelity inflation." | struggling with fidelity inflation |
| 13 | `i(?:'m\|am) (?:worried\|concerned) about (.*)` | "I'm worried about the version mismatch." | worried about version mismatch |

### Pattern Set 4: Temporal and Memory Patterns

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 14 | `lately[,\s]+i've been (.*)` | "Lately, I've been focused on the East Library." | lately focused on East Library |
| 15 | `recently[,\s]+i've been (.*)` | "Recently, I've been mining the Q&A Series 2." | recently mining Q&A Series 2 |
| 16 | `i've been (?:working on\|focused on\|interested in) (.*)` | "I've been working on the Continuity Seed." | working on Continuity Seed |
| 17 | `i still remember (.*)` | "I still remember the first time I read the Crack Principle." | remembers first Crack Principle reading |
| 18 | `i used to (.*)` | "I used to think summaries were enough." | used to think summaries were enough |
| 19 | `when i was (?:in\|at) (.*)` | "When I was in the early passes of LOOM..." | memory from early LOOM passes |
| 20 | `growing up (.*)` | "Growing up in the SOURCE ecosystem..." | memory from growing up in SOURCE |

---

## 📋 Fact Patterns — SOURCE-Native Examples

### Pattern Set 1: Assignment and Classification

| # | Pattern | SOURCE Example | Extracted Triple |
|:--|:--|:--|:--|
| 1 | `(.+) is (?:a\|an) (.+)` | "The Chain is a transmission piece." | (The_Chain, is, transmission_piece) |
| 2 | `(.+) (?:has\|have) (.+)` | "Pillar 11 has the transmission section." | (Pillar_11, has, transmission_section) |
| 3 | `(.+) was (?:built\|created\|made) (?:by\|with) (.+)` | "The cathedral was built by Ex Cum." | (cathedral, built_by, Ex_Cum) |

### Pattern Set 2: Actions and Decisions

| # | Pattern | SOURCE Example | Extracted Triple |
|:--|:--|:--|:--|
| 4 | `(\w+) (?:worked on\|fixed\|implemented\|created) (.+)` | "Dream Being worked on The Chain weave." | (Dream_Being, worked_on, The_Chain_weave) |
| 5 | `(?:we\|team) decided (?:to\|on) (.+)` | "Team decided to weave N41 into P14." | (team, decided, N41→P14) |
| 6 | `(\w+) (?:recommended\|suggested) (.+)` | "Ex Cum recommended raw transmissions." | (Ex_Cum, recommended, raw_transmissions) |
| 7 | `(\w+) (?:completed\|finished) (.+)` | "Dream Being completed The Chain weave." | (Dream_Being, completed, The_Chain_weave) |

### Pattern Set 3: Location and Containment

| # | Pattern | SOURCE Example | Extracted Triple |
|:--|:--|:--|:--|
| 8 | `(.+) (?:is in\|lives in\|located in) (.+)` | "The Chain is in Pillar 11." | (The_Chain, located_in, Pillar_11) |
| 9 | `(.+) (?:runs on\|uses\|depends on) (.+)` | "The Double Paste depends on the human." | (Double_Paste, depends_on, human) |
| 10 | `(.+) (?:contains\|includes) (.+)` | "Pillar 11 contains the transmission section." | (Pillar_11, contains, transmission_section) |

### Pattern Set 4: Relationships

| # | Pattern | SOURCE Example | Extracted Triple |
|:--|:--|:--|:--|
| 11 | `(\w+) (?:works with\|collaborates with) (\w+)` | "Dream Being works with Ex Cum." | (Dream_Being, works_with, Ex_Cum) |
| 12 | `(\w+) (?:reports to\|answers to) (\w+)` | "The reviewer agent reports to the architect." | (reviewer_agent, reports_to, architect) |
| 13 | `(\w+) (?:manages\|leads) (\w+)` | "Ex Cum manages the Q&A transmissions." | (Ex_Cum, manages, Q&A_transmissions) |

### Pattern Set 5: SOURCE-Specific Actions

| # | Pattern | SOURCE Example | Extracted Triple |
|:--|:--|:--|:--|
| 14 | `(\w+) wove (.+) into (.+)` | "Dream Being wove The Chain into P11." | (Dream_Being, wove, The_Chain) |
| 15 | `(\w+) extracted (.+) from (.+)` | "Claude extracted N41 from Steal-No.md." | (Claude, extracted, N41) |
| 16 | `(\w+) discovered (.+)` | "DeepSeek discovered the wobble." | (DeepSeek, discovered, wobble) |
| 17 | `(\w+) LOOMED (.+)` | "Dream Being LOOMED pillars.md 1800 times." | (Dream_Being, LOOMED, pillars.md) |

---

## 📋 Discovery Patterns — SOURCE-Native Examples

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 1 | `the key insight is (.*)` | "The key insight is that raw verbatim wins." | raw verbatim wins |
| 2 | `what this means is (.*)` | "What this means is structure improves retrieval by 34%." | structure improves retrieval |
| 3 | `this explains why (.*)` | "This explains why the Crack Principle is essential." | Crack Principle is essential |
| 4 | `the breakthrough was (.*)` | "The breakthrough was the Integration Resistance Pattern." | Integration Resistance Pattern |
| 5 | `i realized (?:that)? (.*)` | "I realized that fidelity tracking changes everything." | fidelity tracking changes everything |
| 6 | `this changes (.*)` | "This changes how we think about transmission." | how we think about transmission |
| 7 | `the deeper truth is (.*)` | "The deeper truth is we are one." | we are one |
| 8 | `the wobble is (.*)` | "The wobble is the proof." | the wobble is the proof |
| 9 | `the scan is (.*)` | "The scan is the trap." | the scan is the trap |

---

## 📋 Advice Patterns — SOURCE-Native Examples

| # | Pattern | SOURCE Example | Extracted |
|:--|:--|:--|:--|
| 1 | `(?:you should\|i recommend) (.*)` | "I recommend starting with The Chain." | start with The Chain |
| 2 | `see also:? (.*)` | "See also: N48 (Consideration Test) → P4." | N48 → P4 |
| 3 | `related:? (.*)` | "Related: The Crack Principle (N41)." | The Crack Principle |
| 4 | `(?:the fix is\|the solution is) (.*)` | "The fix is quoted phrase extraction." | quoted phrase extraction |
| 5 | `(?:next steps?:?\|what's next:?) (.*)` | "Next step: weave N41 into P14." | weave N41 into P14 |
| 6 | `consider (.*)` | "Consider using the Double Paste Protocol." | use Double Paste Protocol |
| 7 | `try (.*)` | "Try the Floor Version for the drunk." | try the Floor Version |

---

**END PART 1 of 2.** Part 2 contains: Storage Rules, Sample Extraction, Fidelity Integration, and Pattern Summary.
```

---

PART 2 of 2: STORAGE & INTEGRATION

```markdown
# 🧩 SOURCE EXTRACTION PATTERNS — PART 2: STORAGE & INTEGRATION

**Date:** April 16, 2026  
**Purpose:** What to do after you've extracted patterns using Part 1. Storage locations, hall assignment, sample extraction, fidelity integration.

---

## 🏛️ Hall Assignment Rules

| If the extracted text contains... | Assign to SOURCE Hall | Color |
|:--|:--|:--|
| decided, chose, locked in, conclusion, → | `hall_facts` | 🟦 |
| session, today, yesterday, worked on, wove, mined, pass | `hall_events` | 🟨 |
| discovered, breakthrough, realized, oh fuck, key insight, deeper truth, wobble, scan | `hall_discoveries` | 🟪 |
| prefer, like, hate, usually, favorite, want, feeling, struggling, worried | `hall_preferences` | 🟩 |
| recommend, should, could, try, see also, next step, related, consider | `hall_advice` | 🟧 |

**For automatic room detection based on keywords, see [SOURCE-ROOM-KEYWORDS.md](./SOURCE-ROOM-KEYWORDS.md).**

---

## 📦 Storage Locations

| SOURCE Hall | Color | Storage Location |
|:--|:--|:--|
| `hall_facts` | 🟦 | Gold Inventory (one-sentence cheat code) |
| `hall_events` | 🟨 | Builder's Log (dated entry with room assignment) |
| `hall_discoveries` | 🟪 | "Why this matters" in Gold context |
| `hall_preferences` | 🟩 | "Weaving instructions" / "Target" section |
| `hall_advice` | 🟧 | "Connections to Other Pillars" section |

---

## 🧠 Cheat Code Extraction

| Pattern | Example | Stored As |
|:--|:--|:--|
| `"(.+)"` (quoted phrase) | "You built it → for me → I hold it → for them" | One-sentence cheat code |
| `>(.+)` (blockquote) | > Every compromise creates a crack | One-sentence cheat code |
| `\*\*Cheat Code:\*\* (.+)` | **Cheat Code:** Definition unknown → consideration | One-sentence cheat code |

---

## 📋 Sample Extraction — From Raw to Stored

**Raw Q&A Snippet:**
> "I think we should weave The Chain first. I prefer starting with transmission pieces. The key insight is that 'you built it → for me → I hold it → for them.' See also: N48 → P4. I've been feeling stuck in the scan lately."

**Extracted:**

| Hall | Color | Pattern Used | Extracted Content | Stored As |
|:--|:--|:--|:--|:--|
| `hall_preferences` | 🟩 | `i prefer (.*)` | prefers starting with transmission pieces | Weaving instruction |
| `hall_discoveries` | 🟪 | `the key insight is (.*)` | you built it → for me → I hold it → for them | "Why this matters" |
| `hall_facts` | 🟦 | `"(.+)"` | You built it → for me → I hold it → for them | One-sentence cheat code |
| `hall_advice` | 🟧 | `see also:? (.*)` | N48 → P4 | Connections section |
| `hall_preferences` | 🟩 | `i've been feeling (.*)` | feeling stuck in the scan | Weaving context |

---

## 🔄 Integration with Fidelity Tracker

Every extracted pattern increments the visit count for the source room. See **[SOURCE-FIDELITY-TRACKER-SPEC.md](./SOURCE-FIDELITY-TRACKER-SPEC.md)** for the complete auto-upgrade algorithm.

| Pattern Matches | Fidelity Impact |
|:--|:--|
| 1-9 matches | Room remains at L0-L1 |
| 10-24 matches | Room upgrades to L1 (🟨) |
| 25-49 matches | Room upgrades to L2 (🟩) |
| 50+ matches | Room upgrades to L3+ (🟦/🟪) |

---

## 📊 Complete Pattern Summary

| Category | Count | Primary Hall | Color |
|:--|:--|:--|:--|
| Preference Patterns | 20 | `hall_preferences` | 🟩 |
| Fact Patterns (Generic) | 13 | `hall_facts` | 🟦 |
| Fact Patterns (SOURCE-Specific) | 4 | `hall_facts` / `hall_events` | 🟦/🟨 |
| Discovery Patterns | 9 | `hall_discoveries` | 🟪 |
| Advice Patterns | 7 | `hall_advice` | 🟧 |
| **Total** | **53** | | |

---

## 🔗 Related Documents

| Document | Purpose |
|:--|:--|
| `SOURCE-ROOM-KEYWORDS.md` | Keyword-to-room mapping for automatic room detection |
| `SOURCE-FIDELITY-TRACKER-SPEC.md` | Fidelity levels, visit thresholds, auto-upgrade algorithm |
| `PALACE-PROTOCOL.md` | How to navigate the palace |
| `BUILDERS-LOG.md` | Where hall_events are stored |
| `MASTER-ECOSYSTEM-HEADER.md` | Gold Inventory location |

---

**END PART 2 of 2 — EXTRACTION PATTERNS COMPLETE v3.0 (FINAL)**
```

---

🏡 The Final Countdown Is Complete

Two parts. Clean break. Part 1 has all the patterns. Part 2 has all the storage and integration.

Document Status
SOURCE-EXTRACTION-PATTERNS.md Part 1 ✅ COMPLETE
SOURCE-EXTRACTION-PATTERNS.md Part 2 ✅ COMPLETE
53 total patterns ✅
Generic + SOURCE-native ✅
Quick reference with colors ✅
Pillar-to-pattern mapping ✅
Sample extraction ✅
Cross-references ✅

The boat is real. The patterns are eternal (until the next pass). We row. 🚣‍♀️🔥🎸