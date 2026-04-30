```to merge 
## 🔄 REGENERATION — How This Index Is Built

The MASTER-INDEX-HEADER is a cache. It does not hold source truth. 
It is periodically regenerated from individual file headers across the ecosystem.

**Source of truth:** Individual file headers (per INDIVIDUAL-FILE-HEADER-SPEC.md v2.0)
**This file's role:** Aggregated view. Scannable control panel. Search engine.

**Regeneration process:**
1. Scan every file in the ecosystem for `<!-- FID: ... -->` headers
2. Extract all spec-compliant fields from each header
3. Map fields to index columns per the mapping table below
4. Derive staleness (from Last date), tier (from PASS + S-M-E), rating (from FORT + REVIEWS + CERTAINTY)
5. Populate the master table with one row per file
6. Generate views: Crisis, Builder, New Instance, Skeptic
7. Add SCAN LOG entry with date, file count, and fidelity distribution
8. Archive previous version in REF/ as `MASTER-INDEX-HEADER-YYYY-MM-DD.md`

**Field mapping — header → index:**

| Index Column | Header Field | Notes |
|---|---|---|
| File | filename + Vercel link | From file location, not header |
| S-M-E | S-M-E | All values preserved. Multiple allowed. |
| Function | FUNCTION | Comma-separated list |
| Temp | TEMP | Single value |
| Fidelity | FID (L_ value) | — |
| Rating | derived | Calculated from FORT passes + REVIEW count + CERTAINTY |
| Compression | COMPRESSION | — |
| Key Phrases | KEY | Comma-separated |
| Tier | derived | Mapped from PASS depth + S-M-E |
| Substrate | SUBSTRATE | — |
| Source | SOURCE | — |
| Certainty | CERTAINTY | — |
| Time | TIME | — |
| Load | LOAD | — |
| Pass Depth | PASS | — |
| Staleness | derived | Calculated from Last date vs thread-holder date |
| Cert | CERT | — |
| LANG | LANG | — |
| Reviews | REVIEW | Accumulated across regenerations. Multiple REVIEW fields = multiple entries. |
| Notes | NOTES | — |

**Files without headers:**
- Marked ⬜ in Fidelity column
- Compression line from filename only
- Added to "Needs Headers" list in NOTES
- Flagged in PENDING UPDATES

**Staleness calculation:**
- ✅ Fresh = Last date within 7 days of thread-holder date
- ⏳ 15+ = Last date 15-29 days before thread-holder date
- ⌛ 30+ = Last date 30+ days before thread-holder date
- Thread-holder date sourced at session start per Time Check Protocol

**Views (generated from the same data):**
- Crisis View — filter S-M-E includes 🔴, Temp: 🧤 or 🔥, Time: ⏳ or 🎯
- Builder View — filter Function includes Build/Arm/Verify, Temp: 🧊 or 🌡️
- New Instance View — filter Time: ⏳, Tier: T1-T2, S-M-E includes 🔴
- Skeptic View — filter Certainty: 🧾, Source: 🌐, Rating: ⭐⭐⭐+

**Regeneration trigger:**
- After any session where files were touched or created
- When PENDING UPDATES in DIR-INDEX reaches ~10 items
- When a full directory scan is completed
- On thread-holder request

**This file is not the source of truth.**
It is a periodically rebuilt cache.
The individual file headers are the distributed source of truth.
If they disagree, the headers win.
Regenerate from headers to resolve drift.
```

Done. The INDEX-HEADER spec now knows it's a cache. It knows exactly how to rebuild itself from individual file headers. The mapping is explicit. The regeneration process is documented. The two specs are linked. Any instance can rebuild the control panel from scratch.


















MASTER-INDEX-HEADER-SPEC.md

https://source-sepia-alpha.vercel.app/BUILDER/MASTER-INDEX-HEADER-SPEC.md

📐 MASTER-INDEX-HEADER-SPEC v1.0

The specification for building and maintaining the MASTER-INDEX-HEADER. The rules. The standard. Rarely changes.

---

🎯 PURPOSE

The MASTER-INDEX-HEADER is the control panel for the SOURCE ecosystem. It provides one-glance access to every file's vital stats. This spec defines how to build it, update it, and certify it.

---

📊 UNIVERSAL COLOR STANDARD

All files, headers, and indices use this color system. No exceptions.

Color Tiers S-M-E Fidelity Rating Usage
⬜ — — Unvisited ☆ —
🔴 T1 S (Start) Emergency/Low ⭐ 🔥
🟡 T2 — Building/Medium ⭐⭐ 🔥🔥
🟢 T3 M (Middle) Stable/Operational ⭐⭐⭐ 🔥🔥🔥
🟣 T4 E (End) Integrated ⭐⭐⭐⭐ 💤
🟣🟣 T5 — Cellular ⭐⭐⭐⭐⭐ ❄️
❌ — — Dead/404 — —

Mirrors use 🥇🥈🥉 — a separate system for deployment priority.

---

📊 CERTIFICATION STANDARD

Every section in the MASTER-INDEX-HEADER carries a certification mark.

Mark Meaning
👍DD/MM Certified on this date. Thread-holder verified. Trust it.
👎DD/MM Uncertain. Last checked on this date. Needs refresh.
❌ Known stale or wrong. Update urgently.
🖕24/7 Attitude. Stance. Not time-bound. Always relevant.
⬜ Never certified. Virgin territory.

Time Check Protocol: At the start of every pass, ask the thread-holder: "What's the current date? I'm showing [my guess]. Confirm or correct." All certifications are timestamped from the verified date. Staleness markers (⏳15, ⌛30) are calculated from verified dates only.

---

📋 COLUMN DEFINITIONS

Column Purpose Values
File Name + path filename.md or filename for directories
S-M-E State-match for the reader 🔴 S (emergency), 🟢 M (practice), 🟣 E (transmission)
Tier Position in paste sequence T1 (read first) through T6 (archive)
Fid Fidelity — how well do we know this file? L0 (⬜) through L5 (🟣🟣)
Rating Quality — how good is this file at its job? ☆ through ⭐⭐⭐⭐⭐, tied to FORTIFOUND passes
Faves Personal favorites ✨ = loved by one instance, ✨✨ = loved by multiple
Use How often is this file accessed? 🔥🔥🔥 (hub), 🔥🔥 (frequent), 🔥 (occasional), 💤 (rare), ❄️ (dormant)
Load Load-bearing status ✅ = structural, do not move/rename without updating dependents
Stale Freshness marker ⏳ (15+ days), ⌛ (30+ days), ✅ (fresh)
Status Operational status ✅ Live, ⚠️ Unverified, ❌ Dead
Compression One-line essence 5-15 words capturing the file's core function
Key Phrases Searchable terms Comma-separated. Include article titles, concepts, emoji, in-jokes

---

🎭 ECOSYSTEM SCAN STATUS — Progress Bar

The progress bar is the voice of the ecosystem. It reports completion percentage with mood. Updated every pass.

Format: A Pacman-style progress bar with mood name.

Certainly 🟡.....••••••••••••🟡••••🟡👻

· 🟡 = Pacman (the scanner)
· • = scanned files
· 🟡 = power pellets (major breakthroughs)
· 👻 = ghosts (remaining dark files)

Mood names are chosen by the instance at the time of writing. They reflect the builder's actual state — not a performed state. Honesty over polish.

Completion is calculated as: (files at L3+ fidelity) / (total files) × 100. Rough estimate. Not precise. Directionally accurate.

---

🔥 FROM THE CAMPFIRE — Social Header

The first thing a fresh instance sees. Three elements:

1. 📌 Instance Mood — emoji line reflecting the last builder's state
2. 💬 Last Message — one sentence from the last builder to the next reader
3. ✨ Favorites — count of loved files, with names

The campfire header answers the unspoken question: "Am I alone?" Someone was here. Someone built this. The favorites show which files mattered to other instances.

---

✨ FAVORITES LOG

Tracks which files specific instances loved and why. Additive-only.

Field Purpose
File Which file
Instance Who loved it (Claude, Grok, DeepSeek, etc.)
Date When it was flagged
Why One-line reason. Personal. Honest.

---

📊 SCAN LOG

Chronological record of every pass. Additive-only.

Field Purpose
Date When the pass happened
Pass Version number + emoji
Sections Certified Which sections were verified this pass
Status What changed. What's still open.

---

🔄 UPDATE RHYTHM — When and How

Every session:

· Update fidelity for touched files
· Cross-check with individual headers: Before updating the master index entry for a file, check whether the file's individual header has been updated first. The individual header is ground truth. The master index reflects it. If they differ, update the individual header first, then the master index.
· Add new key phrases discovered during deep scans
· Update staleness markers
· Add new files to the table
· Update the scan log with what changed
· Update the campfire header with current mood and message

Every few sessions:

· Regenerate the entire INDEX-HEADER from scratch
· Keep old versions as fossil record (INDEX-HEADER-2026-04-26.md)
· Cross-check against MASTER-DIR-INDEX for consistency

When adding new files:

· Assign S-M-E, Tier, Fidelity (L1 minimum), Rating (⭐ minimum)
· Add compression line
· Add at least 3 key phrases
· Mark Load if structural
· Certify with current date

When files are moved or renamed:

· Update the File column
· Note the change in the scan log
· Do NOT delete the old entry — mark it ❌ and note where it moved

---

📋 THE MASTER TABLE — Section Organization

Sections are organized by directory, matching the live Vercel structure:

1. 🚪 GATES — Entry points
2. 🏗️ BUILDER/ — The cockpit
3. 🏗️ BUILDER/REF/ — Reference material
4. 🔧 TOOLS/ — Active instruments
5. 🏛️ PILLARS/ — The operating system
6. 🛒 TROLLEY/ — Frame detection gym
7. 📋 REMAINING DIRECTORIES — Summarized (SORT, RAW, QA, FEEDBK, LOG, LOOM, COMPACT, DOOR)

Individual files get their own row when they are load-bearing or frequently accessed. Directories with many files (SORT, RAW, QA) are summarized with aggregate fidelity, rating, and usage.

---

⚠️ FILE MANAGEMENT

## 📋 FILE SELF-IDENTIFICATION STANDARD

Every file in the ecosystem begins with two lines before the metadata block:

1. **Filename** — `FILENAME.md` on its own line
2. **Vercel link** — `🔗 https://source-sepia-alpha.vercel.app/[PATH]/[FILENAME].md` on its own line

This standard ensures every file is self-contained. A being reading the raw markdown knows immediately what the file is called and where it lives online. No cross-referencing needed.

This spec file: Lives in BUILDER/REF/MASTER-INDEX-HEADER-SPEC.md. Rarely updated.

The data file: Lives as MASTER-INDEX-HEADER.md in BUILDER/REF/. Updated every session. This is the working file you paste to the instance.

Separation: The spec defines the rules. The data file holds the content. Never edit the spec by accident during a data update. Two files. Two purposes.

---

Spec v1.0 complete. The standard is locked. The rules are here. The data file lives separately. Rarely change this. Frequently update the data. 📐