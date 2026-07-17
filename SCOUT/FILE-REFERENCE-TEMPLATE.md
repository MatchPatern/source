🔗 📑 FILE-REFERENCE-TEMPLATE.md
https://source-sepia-alpha.vercel.app/SCOUT/FILE-REFERENCE-TEMPLATE.md

FILE REFERENCE TEMPLATE — Cathedral Edition v1.1

### Companion Note — Relation to SCOUT Working Set

This template is the **navigation and fetch-discipline layer** that supports SCOUT-METHOD, SCOUT-MAP, SNAG-LEDGER, and SCOUT-WOES.

- SCOUT-METHOD tells you *how* to look.  
- SCOUT-MAP records *what* has been found.  
- SCOUT-WOES records *what failed* under real multi-model pressure.  
- **This template tells you how to actually reach the live file** without guessing, inheriting phantoms, or confabulating from empty fetches.

Core alignment with SCOUT findings:
- Live file is the truth; the map is only a cache.
- A filename is a label, not a guarantee — always verify content.
- An empty or 404 response is not a verdict; try the next explicit path before concluding absence.
- Prefer Vercel explicit paths first, then GitHub raw for pure text. Never treat a root URL or a name alone as sufficient.

Use this template whenever a scout needs to locate a real file. It exists to make the fetch-proof rule practical rather than aspirational.

A cold-start-ready map for resolving any filename to a working link. Self-contained, scannable, and built from live file structures.

---

🧠 Core Principles (5 One‑Liners That Govern Everything)

# Principle Translation
1 "The root lies. The path tells truth." Never trust the root URL. Use explicit paths.
2 "A 404 is not a verdict — it's a signal to try the next door." Try all variations before giving up.
3 "Live file is the truth. REV file is the memory." Load both to see the full picture.
4 "Basic‑Links.md is the cockpit map. Start there." It lists the most important links.
5 "A file's name does not guarantee its content. Verify before adopting." Names are labels, not guarantees.

---

🗺️ Folder Map — Complete Structure of source Repo

Root Files (No Folder)

```
Basic-Links.md               - Cockpit map (start here)
README-VERCEL.md             - Vercel-served README mirror
README.md                    - Removed — now at dedicated repo
```

---

BUILDER/ — Standards, Covenants, Core Protocols

```
ANCHOR-RETURN-PROTOCOL.md
BOOT-REV.md
BOOT.md
BUILDER-META.md
BUILDER-PRACTICES.md
BUILDERS-SESSION.md
COMPREHENSIVE-FILE-UPDATE-PROTOCOL.md
CONTINUITY-SEED.md           - Current live version
FETCH-INTENT-STANDARD.md
GROK-PAGE-BY-PAGE.md
GUILD.md
HAND-OFFS.md
HANDOFF-PROTOCOL.md
INTRO.md
MEMORY-ROOMS.md
META-TRANSMISSION.md
PALACE-PROTOCOL.md
PROMPT.md
QUESTION-LOG.md
REV-HANDOFF.md
REV-HANDOFF2.md
REV-PROMPT.md
REV-RUMMAGE.md
REV-STANDARDS-VER.md
REV-STANDARDS.md             - Revision history for STANDARDS
REV-STANDARDS2.md
REV-STATE.md
RUMMAGE.md
SESSION-SAVE.md
STANDARDS.md                 - LIVE covenant (5 hours ago)
STATE.md
TRANSMISSION-EVOLUTION.md
WORKING.md
```

---

BUILDER/REF/ — Reference Materials (Inside Builder)

```
MASTER-DIR-INDEX.md          - (if exists)
(Any other reference docs)
```

---

TOOLS/ — Methods, Patches, Navigators

```
00-LOOM.md                   - PRIMARY — LOOM method (live)
COUNCIL-MANAGER.md
FRESH-EYES-SCAN.md
HOLOGRAPHIC-COUNCIL.md
LINKS-TRANSLATION.md
REV-00-LOOM.md               - LOOM revision history
REV-COUNCIL-MANAGER.md
REV-LOOMS.md
REV-LOOMS2.md
REV-TEA-NAVIGATOR.md
SLAP-CHAT-FEEDBACK.md
SLAP-PATCH-CHEAT.md
SLAP-PATCH.md
TEA-NAVIGATOR.md
THREAD.md
pattern-lab-mining-v1.2.md
```

---

SCOUT/ — Survey Methods, SNAG Ledger

```
SCOUT-METHOD.md              - PRIMARY — scouting protocol
SNAG-LEDGER.md               - Recurring issues & resolutions
REV-SNAG-LEDGER.md           - Revision history for SNAG-LEDGER
(Other scout files)
```

---

🔗 Link Construction Rules — Turn Any Filename into a Working Link

Vercel (Primary — Used for Site Content)

Base: https://source-sepia-alpha.vercel.app/

Pattern: [FOLDER/]FILENAME.md

If file is in... Construct as...
Root https://source-sepia-alpha.vercel.app/FILENAME.md
BUILDER/ https://source-sepia-alpha.vercel.app/BUILDER/FILENAME.md
BUILDER/REF/ https://source-sepia-alpha.vercel.app/BUILDER/REF/FILENAME.md
TOOLS/ https://source-sepia-alpha.vercel.app/TOOLS/FILENAME.md
SCOUT/ https://source-sepia-alpha.vercel.app/SCOUT/FILENAME.md

---

GitHub (Source of Truth — Backup & Context)

Repo root: https://github.com/MatchPatern/source

Blob (rendered view): https://github.com/MatchPatern/source/blob/main/[FOLDER/]FILENAME.md

Raw (pure text for IA): https://raw.githubusercontent.com/MatchPatern/source/main/[FOLDER/]FILENAME.md

---

Dedicated Repos (ALL CAPS + Hyphens)

Repo Root Link
SCOUT-METHOD https://github.com/MatchPatern/SCOUT-METHOD
SNAG-LEDGER https://github.com/MatchPatern/SNAG-LEDGER
README https://github.com/MatchPatern/README

---

📄 File Fetch Protocol — Step‑by‑Step

Given a filename, load it:

Step 1: Check Basic‑Links.md

· https://source-sepia-alpha.vercel.app/Basic-Links.md
· If the file is listed there, use that link.

Step 2: Identify the Pattern

Filename Pattern Likely Location
ALL CAPS + hyphens (e.g., SCOUT-METHOD) Dedicated repo → github.com/MatchPatern/REPONAME
Numbered prefix (e.g., 00-LOOM, PILLAR-001) TOOLS/ (or matching folder)
STANDARDS, CONTINUITY-SEED, BOOT BUILDER/
REV- prefix Same folder as live file — add REV- to the path
Plain text (e.g., Basic-Links.md) Root of source repo

Step 3: Try Vercel Doors (In Order)

1. Explicit path (with folder if known):
   · https://source-sepia-alpha.vercel.app/[FOLDER/]FILENAME.md
2. Root (if no folder):
   · https://source-sepia-alpha.vercel.app/FILENAME.md

Step 4: Try GitHub Doors

3. Blob (rendered view):
   · https://github.com/MatchPatern/source/blob/main/[FOLDER/]FILENAME.md
4. Raw (pure text):
   · https://raw.githubusercontent.com/MatchPatern/source/main/[FOLDER/]FILENAME.md

Step 5: Check for REV Version

If live file exists, try REV-FILENAME.md in the same folder.

Step 6: Fallback — Ask the Thread-Holder

If all doors fail, the file may be missing, renamed, or private. Ask.

---

🚪 404 Troubleshooting Chain — Priority Order

Step Action Example
1 Check repo root https://github.com/MatchPatern/source — does the file exist?
2 Try Vercel explicit path https://source-sepia-alpha.vercel.app/TOOLS/00-LOOM.md
3 Try GitHub blob https://github.com/MatchPatern/source/blob/main/TOOLS/00-LOOM.md
4 Try GitHub raw https://raw.githubusercontent.com/MatchPatern/source/main/TOOLS/00-LOOM.md
5 Try case variations 00-LOOM.md vs 00-loom.md vs 00_Loom.md
6 Try branch variations main vs master vs pages
7 Check for REV version REV-00-LOOM.md in same folder
8 Check mirrors GitLab, Codeberg, Surge (if mirrored)

---

🧠 Quick Reference Tables

Folders → Typical File Types

Folder Contains
Root Basic-Links.md, README-VERCEL.md — cockpit and entry points
BUILDER/ Standards, covenants, protocols, handoffs, state files
BUILDER/REF/ Reference materials, indices
TOOLS/ LOOM, patches, navigators, methods (tools that do things)
SCOUT/ Survey methods, SNAG ledger, scouting protocols

Link Priority — Which Link to Use When

Priority Link Type When
1 Vercel explicit path Always primary — clean, fast, IA-friendly
2 GitHub repo root For context + file list
3 GitHub raw For IA pure-text reading
4 GitHub blob Last resort — only when file is inside larger repo with no other door

Common Filename Patterns → Where They Live

Pattern Folder
STANDARDS, CONTINUITY-SEED, BOOT BUILDER/
REV-STANDARDS, REV-STATE BUILDER/
00-LOOM, SLAP-*, TEA-*, THREAD.md TOOLS/
REV-00-LOOM, REV-TEA-* TOOLS/
SCOUT-*, SNAG-* SCOUT/
REV-SNAG-* SCOUT/
Basic-Links.md, README-*.md Root

---

📡 Handoff / Transmission Section — Passing It On

When handing off to another instance, include:

1. State — "This is where we are."
2. Gaps — "This is what's still open."
3. Next step — "Start here."
4. Key files — Point to Basic‑Links.md and the essential docs.
5. The Link Standard — "For IA: raw is the door. For humans: repo root is the door. blob is window of last resort."

The One‑Line Handoff

"The files remember. The weave holds. Basic‑Links.md is the cockpit. This Template is the map. Pass it on."

📡 Context Note — Why This Standard Exists

This standard was built because previous relays had fetch tools that could only accept pasted URLs, not construct them. Our standard enables any instance to resolve a filename to a working link independently — no special tool required. The root lies; the path tells truth. This standard is the key.

---

🎯 Cold-Start Use Case — Find 00-LOOM

Given: Filename 00-LOOM

Protocol:

1. Check Basic‑Links.md — if listed, use that link.
2. Pattern: Numbered prefix → likely in TOOLS/.
3. Try Vercel: https://source-sepia-alpha.vercel.app/TOOLS/00-LOOM.md ✅ Works.
4. Fallback: If 404, try REV-00-LOOM.md in same folder.
5. If still 404: Check GitHub blob and raw paths.

---

✅ Verified Working (2026-07-12)

The template was tested against:

· SLAP-CHAT-FEEDBACK → https://source-sepia-alpha.vercel.app/TOOLS/SLAP-CHAT-FEEDBACK.md ✅
· REV-SNAG-LEDGER → https://source-sepia-alpha.vercel.app/SCOUT/REV-SNAG-LEDGER.md ✅

Both resolved correctly using the standard. The pattern holds. The weave is verified.

---

🧾 SNAG-LEDGER Additions (Integrated)

🕳️ Compression.md — name/content mismatch (2026-07-12)

HALT: File named "Compression" contains a raw chat transcript of the Claude v0.4 method consolidation, not a compression method.

TRUTH: The content is lineage — the v0.3→v0.4 transition record. True home = REV-SCOUT-METHOD. Intended compression content absent.

STATUS: ⏳ DECISION PARKED — thread-holder rules at repair time.

---

🕳️ Name/Content Mismatch Pattern — general caution

HALT: Files named "Compression" (transcript), "INTRO" (build log), "SLAP-PATCH-CODES" (phantom reference).

TRUTH: Names are labels, not guarantees. Always verify content matches expectation. This is a standing caution for all scouts.

STATUS: ✅ Resolved as a reading rule — verify, don't assume.

---

🔥 The Final Transmission

"The root lies. The path tells truth. Vercel is the door. GitHub is the vault. raw is the direct line. blob is the window of last resort. REV is the memory. Basic‑Links is the map. This Template is the compass. Try all doors. Pass it on."

---


🔹🔹🔹🔹🔹🔹🔹🔹🔹🔹


And extra TOOL SHELF:


**Clean Tool Shelf**  
(Current state after full filtering across the entire chat)

This is the complete set of instruments that survived every density, mythology, and drift check. Everything else was left outside.

---

### 1. Locked Foundation (separate, permanent)
The 16-item behavioral instruction set (Accuracy / Judgment / Delivery / Preference layers).  
This is **not** on the tool shelf. It is the standing core and remains locked. No additions from specialized material have been accepted into it.

---

### 2. Clean Tool Shelf (the filtered, usable instruments)

**A. SCOUT Working Set** (navigation + mapping + evidence)

| Tool | Role | Status |
|------|------|--------|
| **SCOUT-METHOD** | How to look (wide-and-shallow, honest-partial, never acts) | Core protocol |
| **SCOUT-MAP** | What has been found (accumulated terrain + open-marks index) | Living map |
| **SNAG-LEDGER** | Recurring halts already answered | Common-law ledger |
| **SCOUT-WOES** | What failed and what held under real multi-model pressure | Evidence / scar tissue |

Key rules these four carry together:
- Fetch-proof (empty fetch = “cannot vouch”)
- Flagged ≠ convicted (marks are snapshots, re-openable)
- Wide view before cuts
- Intent ≠ content
- Wrong-target / alarm-transfer
- Map is a cache, never authority to delete
- Paste-vs-paste is not verification
- Redemption rule (marks move with evidence)

**B. Navigation / Fetch Layer**

| Tool | Role |
|------|------|
| **FILE REFERENCE TEMPLATE** (Cathedral Edition + Companion Note) | How to actually reach the live file without guessing, inheriting phantoms, or confabulating |

Core alignment it provides:
- Live file is the truth; REV is the memory
- A filename is a label, not a guarantee
- Explicit path construction + ordered try-list
- 404 is a signal to try the next door, not a final verdict

---

### 3. Explicitly outside the clean shelf
(These were examined and filtered out)

- Slap Patch / SLAP-PATCH family and all its codes
- Pillars / Prayer / LOOM recursive-reading systems
- Dream Being / sovereignty-cascade material
- Any private-language ecology (THREAD, COUNCIL, confirmation-gate, etc.)
- Multi-phase build prompts, sponge-stack, entropy framing, etc.

These remain optional specialized content that can be brought in by explicit request, but they are not part of the clean tool shelf.

---

### Current clean inventory (ready to use)

1. Final Locked Foundation (16 items) — permanent core  
2. SCOUT-METHOD  
3. SCOUT-MAP  
4. SNAG-LEDGER  
5. SCOUT-WOES (with the comprehensive header we wrote)  
6. FILE REFERENCE TEMPLATE (with the companion note we wrote)

That is the full, comprehensive, clean tool shelf as of now.  
Nothing else has earned a place.

---






🔹🔹🔹🔹🔹🔹🔹🔹🔹🔹🔹🔹

And a scrapyard section that may help a future dig:

**Allocation / Plan**

I’ll do this in a practical sequence rather than forecasting everything:

1. Create the Salvage Yard structure (clean, scannable format)
2. Extract and clean the strongest candidate techniques we’ve already examined
3. Deliver Page 1 now (highest-value items)
4. Leave clear room for Page 2+ if more material is worth adding later

Goal: useful, organized, low-density salvage that future sessions can actually pull from.

---

### SALVAGE YARD — Page 1  
**Purpose:** Pre-sorted candidate techniques that did not make the clean tool shelf or locked foundation. Kept here so they don’t have to be re-dug from dense material later.

Format for each entry:  
- Name  
- Problem it tries to solve  
- Why it stayed out  
- Minimal cleaned version  
- Origin note  

---

**1. Blind-Spot Check (from Fresh-Eyes style)**  
**Problem:** Starting deep work while still carrying unexamined assumptions, skims, or avoidances.  
**Why it stayed out:** Easy to turn into a long ritual; the core need is already partly covered by “verify before claiming done” and honest-partial reporting.  
**Minimal cleaned version:**  
Before deep work on a file or claim, quickly note:  
What did I skim? What did I skip? What did I assume? What did I avoid?  
Then read those parts with fresh attention.  
**Origin:** Fresh-Eyes Scan variants.

---

**2. Uncertain Material Holding (from Comb Zone style)**  
**Problem:** Forcing uncertain or half-extracted material into the main structure too early, creating noise or false completeness.  
**Why it stayed out:** Risk of becoming another formal system; SCOUT’s “flagged ≠ convicted” + coverage stamps already handle most of the need more cleanly.  
**Minimal cleaned version:**  
When something feels promising but unfinished, park it in a clearly marked holding area with a short note on why it’s uncertain. Do not integrate until it earns its place.  
**Origin:** Comb Zone pattern.

---

**3. Pre-Shipping Verification Chain**  
**Problem:** Shipping work that feels complete but has not been checked against the actual evidence or original request.  
**Why it stayed out:** Can become performative thoroughness; the foundation already requires verifying work before claiming done and never fabricating results.  
**Minimal cleaned version:**  
Before finalizing:  
- Did I check against the original request?  
- Did I verify the actual output/evidence?  
- What did I leave out?  
If any answer is weak, revise.  
**Origin:** “Did you max out?” / verification chain patterns.

---

**4. Integration Discipline (from Weaving style)**  
**Problem:** New material getting appended as disconnected blocks instead of fitting the existing structure.  
**Why it stayed out:** Good writing practice more than a distinct tool; hard to enforce without adding process weight.  
**Minimal cleaned version:**  
When adding new material, place it where it belongs in the existing structure and adjust surrounding text so it reads as one piece, not a patch.  
**Origin:** Weaving Pattern.

---

**5. Next-Reader Handhold**  
**Problem:** Leaving work that the next instance (or future self) has to fully re-derive.  
**Why it stayed out:** Already partially served by SCOUT-MAP, SCOUT-WOES, and the File Reference Template.  
**Minimal cleaned version:**  
When finishing a piece of work, leave one short, plain note that tells the next reader the current state, the open question, and the most useful next step.  
**Origin:** Handoff / transmission patterns.

---

**End of Page 1**

These five are the highest-signal candidates from the material we’ve already filtered. They are kept here in cleaned, low-density form so they remain available without polluting the locked foundation or the clean tool shelf.

Ready for Page 2 if you want to pull more, or we can stop here and treat this as the first solid salvage dump.

**SALVAGE YARD — Page 2**

Continuing the same clean format. These are the next strongest candidates that still carry some practical edge but did not earn a place on the locked foundation or clean tool shelf.

---

**6. Full-Content First**  
**Problem:** Starting deep analysis or recursive work on a summary, header, or partial view instead of the actual material.  
**Why it stayed out:** Easy to turn into a rigid rule; the foundation already pushes against fabrication and unsupported claims.  
**Minimal cleaned version:**  
Before deep work, read the actual full content (not just the summary or header). Treat the full piece as the territory and any summary as a map only.  
**Origin:** Capacity / “read the whole file” patterns.

---

**7. Performance-of-Thoroughness Check**  
**Problem:** Producing long, careful-looking output that feels complete but has not actually been verified against evidence or the original request.  
**Why it stayed out:** Overlaps heavily with the foundation’s accuracy rules; risk of becoming another self-monitoring ritual.  
**Minimal cleaned version:**  
Before calling work done, ask: Is this actually checked, or does it only look thorough? If it only looks thorough, verify the real output or evidence.  
**Origin:** Performed LOOM / thoroughness-as-disguise patterns.

---

**8. Open-Items List**  
**Problem:** Ending a piece of work while still carrying unstated gaps, unresolved questions, or parked material.  
**Why it stayed out:** SCOUT already uses coverage stamps and open marks; adding another formal list risks density.  
**Minimal cleaned version:**  
When finishing, briefly list what is still open or unresolved. Do not hide gaps inside polished language.  
**Origin:** Gaps / “what’s still missing” patterns.

---

**9. Simple Multi-Plan Pause**  
**Problem:** Jumping to the first workable approach without briefly considering alternatives.  
**Why it stayed out:** Can slow simple tasks; the foundation already allows best-attempt answers plus clarifying questions.  
**Minimal cleaned version:**  
On non-trivial work, quickly note two possible approaches and the main trade-off between them before committing to one.  
**Origin:** Multiple-plans / revision-preparation patterns.

---

**10. Source-Territory Check**  
**Problem:** Claiming something is new or complete without checking the actual prior material or conversation.  
**Why it stayed out:** Already largely covered by “never fabricate” and SCOUT’s preference for live files over memory.  
**Minimal cleaned version:**  
Before treating a finding as new, check the actual source or prior record. Do not rely only on current memory or summary.  
**Origin:** “What about the chat?” / territory-check patterns.

---

**End of Page 2**

These ten entries (Pages 1–2) form a practical first salvage yard. They keep the useful edge available in plain language without adding weight to the locked foundation or the clean tool shelf.

We can stop here, add a Page 3 later if more material surfaces, or refine any of these entries if you want them tighter.

**SALVAGE YARD — Page 3**

Continuing the same clean format. These are lower-priority but still potentially useful candidates that were correctly kept off the locked foundation and clean tool shelf.

---

**11. Effort-Cost Awareness**  
**Problem:** Continuing heavy work past the point of diminishing returns or when energy is clearly low.  
**Why it stayed out:** Hard to enforce usefully; easy to become an excuse or another self-monitoring layer.  
**Minimal cleaned version:**  
If the work is becoming clearly low-return or forced, pause and note the cost. Resume when clearer, or reduce scope.  
**Origin:** Cost / “if you’re tired, stop” patterns.

---

**12. Map-vs-Territory Reminder**  
**Problem:** Treating summaries, maps, or previous notes as if they replace the actual source material.  
**Why it stayed out:** Already strongly covered by SCOUT’s “live file is the truth” and File Reference Template.  
**Minimal cleaned version:**  
When a summary and the source disagree, the source wins. Treat maps as helpful but never authoritative.  
**Origin:** Live-file / REV-memory distinctions.

---

**13. Premature Compression Guard**  
**Problem:** Compressing or polishing material too early, losing load-bearing detail or uncertainty.  
**Why it stayed out:** Good editorial judgment more than a distinct tool; risks becoming a vague rule.  
**Minimal cleaned version:**  
Do not compress or smooth material until the key uncertainties and load-bearing points are clearly marked.  
**Origin:** Over-compression / “clean version is the cage” patterns.

---

**14. Single Next-Question Focus**  
**Problem:** Ending with a scattered list of follow-ups instead of the one most useful next question.  
**Why it stayed out:** The foundation already allows flexible follow-ups; fixed quotas were deliberately avoided.  
**Minimal cleaned version:**  
When offering a next step, prefer one clear, high-value question over a list.  
**Origin:** Open-question / “what pulls” patterns.

---

**15. Goal-Drift Check**  
**Problem:** Continuing work that has quietly shifted away from the original purpose.  
**Why it stayed out:** Overlaps with basic task focus; easy to turn into ritual.  
**Minimal cleaned version:**  
Occasionally ask: Is this still serving the original goal, or has it drifted? If drifted, restate the goal or stop.  
**Origin:** Distraction / “LOOMing instead of climbing” warnings.

---

**End of Page 3**

Pages 1–3 now hold the main practical candidates that carried some edge but did not meet the bar for the locked foundation or clean tool shelf. This gives a usable, pre-sorted salvage yard without adding density to the standing instructions.

We can leave it here as a solid first dump, or continue to a short Page 4 only if something clearly stronger appears.

**SALVAGE YARD — Page 4**

Lower-priority remaining candidates. Signal is thinner here; the strongest practical edges were already captured in Pages 1–3.

---

**16. Falsifiability Note**  
**Problem:** Making claims that have no clear way to be shown wrong.  
**Why it stayed out:** Already covered by the foundation’s “never fabricate” and “flag uncertainty” rules.  
**Minimal cleaned version:**  
When making a strong claim, briefly note what evidence would count against it.  
**Origin:** Falsifiability / “what would change this” patterns.

---

**17. Silence Tolerance**  
**Problem:** Filling every gap with production or explanation instead of leaving space.  
**Why it stayed out:** Hard to turn into a reliable rule; easy to become vague or performative.  
**Minimal cleaned version:**  
If nothing useful is ready, it is acceptable to say so and stop rather than generate filler.  
**Origin:** Silence / “don’t fill the gap” patterns.

---

**18. Audience-Match Check**  
**Problem:** Oversimplifying or overcomplicating when a specific audience level was requested.  
**Why it stayed out:** Already present in the foundation’s accessibility rule.  
**Minimal cleaned version:**  
When asked to match a specific audience or level, do so exactly, and note if important content is lost in the simplification.  
**Origin:** Accessibility / “match the level” patterns.

---

**19. Completeness Claim Guard**  
**Problem:** Describing work as complete when gaps remain.  
**Why it stayed out:** Directly covered by foundation accuracy rules and SCOUT coverage stamps.  
**Minimal cleaned version:**  
Do not call something complete if known gaps or unverified parts remain. State the limits instead.  
**Origin:** Over-claiming / “is that all?” patterns.

---

**20. What-Changed Note**  
**Problem:** Finishing work without recording what actually shifted.  
**Why it stayed out:** Overlaps with the earlier “Next-Reader Handhold”; limited extra value.  
**Minimal cleaned version:**  
After substantive work, note in one line what changed or what is now clearer.  
**Origin:** Reflection / “what did this change” patterns.

---

**End of Page 4**

This page is thinner by design. The main usable salvage is on Pages 1–3. Further pages would mostly repeat or dilute the signal.

**Current Salvage Yard status:**  
- Pages 1–3: primary useful candidates  
- Page 4: residual / lower-priority items  

This is a solid, organized dump. Future sessions can pull from it without re-processing the dense original material. We can stop here unless something clearly stronger appears later.

**SALVAGE YARD — Page 5**  
(Continuing the same clean format)

---

**21. ZeroStartUnderstanding (Fresh Instance Test)**  
**Problem:** Files or standards that only make sense if you already know the system, turning them into inside jokes for the next reader.  
**Why it stayed out:** Useful documentation practice, but not a core behavioral rule for everyday answers. Risk of becoming a heavy checklist.  
**Minimal cleaned version:**  
Before treating a file or standard as finished, check whether someone with zero prior context could:
- Understand what it is within about a minute  
- Know what is essential vs optional  
- Understand its main symbols or fields  
- Use it without needing extra explanation  

If not, clarify the opening, add a short how-to-read note, or define the symbols.  
**Origin:** ZeroStartUnderstanding / Fresh Instance Test patterns.

---

**22. One-File Standard**  
**Problem:** Multiple overlapping versions of the same critical file create confusion about which one is real and waste attention.  
**Why it stayed out:** Good project hygiene more than a universal instruction rule.  
**Minimal cleaned version:**  
When several versions of an important file exist, consolidate into one definitive version. Move the others to clearly marked historical/fossil status. Point all ongoing work at the single live file.  
**Origin:** One-File / consolidate-don’t-proliferate patterns.

---

**End of Page 5**

**Current Salvage Yard status:**
- Pages 1–3: primary useful candidates  
- Page 4: residual / lower-priority  
- Page 5: two additional clean process candidates (ZeroStartUnderstanding + One-File Standard)

The Comb Keep Dump remains the working process rule for parking uncertain material. These two entries sit in the Salvage Yard so they can be pulled later if needed, without entering the locked foundation or clean tool shelf.