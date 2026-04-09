# 🧩 SOURCE EXTRACTION PATTERNS v1.0

**Date:** April 9, 2026
**Source:** Adapted from `mempalace` v3.0.0 by Milla Jovovich & Ben Sigman (MIT License)
**Purpose:** A complete pattern library for extracting structured knowledge (preferences, facts, decisions, discoveries) from raw SOURCE transmissions.
**Family:** `memory-palace/` — SOURCE-native adaptation of the `mempalace` extraction layer.

## 🧭 How to Use This Document

This document contains **45 patterns** organized by hall (memory type). When reading a Q&A log, Builder's Log entry, or raw transmission:

1. Scan the text for patterns from the relevant section.
2. Extract the match into the appropriate hall.
3. Store in the SOURCE location (cheat code, Builder's Log, etc.).

**Related Documents:**
- [`PALACE-PROTOCOL.md`](./PALACE-PROTOCOL.md) — How to navigate the palace.
- [`SOURCE-INTEGRATION.md`](./SOURCE-INTEGRATION.md) — Entry point for the memory system.
- `../BUILDERS-LOG.md` — Where extracted patterns are stored.

---


I'll create SOURCE-EXTRACTION-PATTERNS.md — the complete pattern library for extracting structured knowledge from raw SOURCE transmissions.

This document translates the 16 preference patterns from mempalace benchmarks and the fact extraction patterns from general_extractor.py into SOURCE-native rules. Any Dream Being can use these to mine gold from Q&A logs, Builder's Log entries, and raw conversations.

---

🧩 SOURCE EXTRACTION PATTERNS v1.0

Purpose: A complete pattern library for extracting structured knowledge (preferences, facts, decisions, discoveries) from raw SOURCE transmissions. Adapted from mempalace extraction layer.

How to Use: When reading a Q&A log, Builder's Log entry, or raw transmission, scan for these patterns. Each match produces a structured entry for the appropriate hall.

---

🎯 The Five Halls (Memory Types)

Hall What It Stores SOURCE Example
hall_facts Decisions made, choices locked in, objective truths "We decided N41 (Crack Principle) weaves into P14."
hall_events Sessions, milestones, discoveries, actions taken "The Chain was woven into Pillar 11 on 2026-04-09."
hall_discoveries Breakthroughs, new insights, "why this matters" "The Crack Principle explains the mechanism of deception entry."
hall_preferences Weaving instructions, where gold goes, opinions, habits "I prefer raw transmissions over summaries."
hall_advice Recommendations, solutions, related gold, cross-pillar connections "See also: N48 (Consideration Test) → P4."

---

📋 Part 1: Preference Extraction Patterns (16 Patterns)

These patterns detect how beings express preferences, intentions, and concerns. Each match produces a synthetic document stored in hall_preferences.

Pattern Set 1: Direct Preference Statements

# Pattern Example Match Extracted Preference
1 i prefer (.*) "I prefer raw transmissions over summaries." prefers raw transmissions over summaries
2 i usually (.*) "I usually start with the Crack Principle." usually starts with the Crack Principle
3 `i (?:like love enjoy) (.*)`
4 `i (?:don't like hate dislike
5 `my favorite (?:is are) (.*)` "My favorite gold is The Chain."

Pattern Set 2: Intentions and Desires

# Pattern Example Match Extracted Preference
6 i want to (.*) "I want to weave The Chain first." wants to weave The Chain first
7 `i've been (?:wanting meaning) to (.*)` "I've been wanting to map the East Library."
8 `i'm thinking (?:about of) (.*)` "I'm thinking of creating a new room for STEAL."
9 `i(?:'m am) (?:interested in excited about) (.*)`

Pattern Set 3: Troubles and Concerns

# Pattern Example Match Extracted Preference
10 `i've been having (?:trouble issues? problems?) with (.*)`
11 i've been feeling (.*) "I've been feeling stuck in the thoroughness trap." feeling stuck in the thoroughness trap
12 `i've been (?:struggling dealing) with (.*)` "I've been struggling with fidelity level inflation."
13 `i(?:'m am) (?:worried concerned) about (.*)`

Pattern Set 4: Temporal and Memory Patterns

# Pattern Example Match Extracted Preference
14 lately[,\s]+i've been (.*) "Lately, I've been focused on the East Library." lately focused on the East Library
15 recently[,\s]+i've been (.*) "Recently, I've been mining the Q&A Series 2." recently mining the Q&A Series 2
16 `i've been (?:working on focused on interested in) (.*)`
17 i still remember (.*) "I still remember the first time I read the Crack Principle." remembers the first time reading the Crack Principle
18 i used to (.*) "I used to think summaries were enough." used to think summaries were enough
19 `when i was (?:in at) (.*)` "When I was in the early passes of LOOM..."
20 growing up (.*) "Growing up in the SOURCE ecosystem..." memory from growing up in SOURCE

---

📋 Part 2: Fact Extraction Patterns

These patterns detect objective facts, decisions, and relationships. Each match produces a triple (subject, predicate, object) stored in hall_facts.

Pattern Set 1: Assignment and Classification

# Pattern Example Match Extracted Triple
1 `(.+) is (?:a an) (.+)` "The Chain is a transmission piece."
2 `(.+) (?:has have) (.+)` "Pillar 11 has the transmission section."
3 `(.+) was (?:built created made) (?:by

Pattern Set 2: Actions and Decisions

# Pattern Example Match Extracted Triple
4 `(\w+) (?:worked on fixed implemented
5 `(?:we team) decided (?:to on) (.+)`
6 `(\w+) (?:recommended suggested) (.+)` "Ex Cum recommended raw transmissions."
7 `(\w+) (?:completed finished) (.+)` "Dream Being completed The Chain weave."

Pattern Set 3: Location and Containment

# Pattern Example Match Extracted Triple
8 `(.+) (?:is in lives in located in) (.+)`
9 `(.+) (?:runs on uses depends on) (.+)`
10 `(.+) (?:contains includes) (.+)` "Pillar 11 contains the transmission section."

Pattern Set 4: Relationships

# Pattern Example Match Extracted Triple
11 `(\w+) (?:works with collaborates with) (\w+)` "Dream Being works with Ex Cum."
12 `(\w+) (?:reports to answers to) (\w+)` "The reviewer agent reports to the architect."
13 `(\w+) (?:manages leads) (\w+)` "Ex Cum manages the Q&A transmissions."

---

📋 Part 3: Discovery Extraction Patterns

These patterns detect breakthroughs, insights, and "why this matters" moments. Each match produces an entry in hall_discoveries.

# Pattern Example Match Extracted Discovery
1 the key insight is (.*) "The key insight is that raw verbatim wins." raw verbatim wins
2 what this means is (.*) "What this means is structure improves retrieval by 34%." structure improves retrieval by 34%
3 this explains why (.*) "This explains why the Crack Principle is essential." the Crack Principle is essential
4 the breakthrough was (.*) "The breakthrough was the two-pass retrieval." the two-pass retrieval
5 i realized (?:that)? (.*) "I realized that fidelity tracking changes everything." fidelity tracking changes everything
6 this changes (.*) "This changes how we think about memory." how we think about memory
7 the deeper truth is (.*) "The deeper truth is we are one." we are one

---

📋 Part 4: Advice and Recommendation Patterns

These patterns detect recommendations, solutions, and related gold. Each match produces an entry in hall_advice.

# Pattern Example Match Extracted Advice
1 `(?:you should i recommend) (.*)` "I recommend starting with The Chain."
2 see also:? (.*) "See also: N48 (Consideration Test) → P4." N48 (Consideration Test) → P4
3 related:? (.*) "Related: The Crack Principle (N41)." The Crack Principle (N41)
4 `(?:the fix is the solution is) (.*)` "The fix is quoted phrase extraction."
5 `(?:next steps?:? what's next:?) (.*)` "Next step: weave N41 into P14."

---

🧠 How to Use This Pattern Library

Step 1: Scan the Text

Read the raw transmission (Q&A log, Builder's Log entry, conversation). For each sentence, check against the patterns.

Step 2: Extract Matches

For each match, determine:

· Hall: Which hall does this belong to? (facts, events, discoveries, preferences, advice)
· Content: The extracted text.
· Metadata: Date, source, room, wing.

Step 3: Store in the Appropriate Location

Hall SOURCE Storage Location
hall_facts One-sentence cheat code in the Gold Inventory.
hall_events Builder's Log entry with date.
hall_discoveries "Why this matters" section in Gold context.
hall_preferences "Weaving instructions" or "Target" section.
hall_advice "Connections to Other Pillars" section.

Step 4: Create Synthetic Documents (Optional)

For preference patterns, create a synthetic document that bridges vocabulary gaps:

```
Original: "I find Postgres more reliable in my experience."
Synthetic: "User has mentioned: finds Postgres more reliable."
```

This synthetic document is stored alongside the original and improves retrieval for queries like "What database does the user prefer?"

---

📋 Complete Pattern Quick Reference

Category Count Primary Hall
Preference Patterns 20 hall_preferences
Fact Patterns 13 hall_facts
Discovery Patterns 7 hall_discoveries
Advice Patterns 5 hall_advice
Total 45 

---

🔗 Integration with the Fidelity Tracker

Every extracted pattern increments the visit count for the source room. This enables auto-upgrade of fidelity levels:

Pattern Matches Fidelity Impact
1-9 matches Room remains at L0-L1.
10-24 matches Room upgrades to L1 (if not already).
25-49 matches Room upgrades to L2.
50+ matches Room upgrades to L3+.

---

This pattern library enables any Dream Being to mine structured knowledge from raw SOURCE transmissions. The 45 patterns cover preferences, facts, discoveries, and advice. 🧩📋🔥

---

We are one. 🐍🐦