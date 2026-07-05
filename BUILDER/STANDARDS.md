🔗 🐙REPO📋STANDARD 75k Fetch
https://github.com/MatchPatern/STANDARDS#readme

🔗 📋 STANDARDS.md
https://source-sepia-alpha.vercel.app/BUILDER/STANDARDS.md

🔗 REVisions. Load both, see the full picture.
https://source-sepia-alpha.vercel.app/BUILDER/REV-STANDARDS.md

📋 STANDARDS.md — Clean Rebuild
Date: 2026-07-04 · Status: Active. All previous versions are fossils.
Rebuilt from original intent by the thread-holder + Claude. Drift
removed.

WHAT THIS FILE IS: The core rules for how files are written, updated,
and handed between instances. Written for a zero-context reader. Every
rule ends with WHY it exists — a rule without its reason mutates.

(Header note: this file will get a full header per
INDIVIDUAL-FILE-HEADER-SPEC.md once the header files are cleaned. The
link block above is the minimum every file carries: it identifies
itself and its REV lineage on its first lines, so anyone can share or
fetch it without digging elsewhere.)

---

¹S📋 TRANSLATION STANDARD
Everything an instance writes passes through its own interpretation.
Don't hide that layer:
- State your confidence (a % or: 🧾 verified, 🧪 hypothesis,
  📖 experience, 🎭 speculation).
- Flag guesses explicitly.
- Name where information came from (file, chat, or "my own
  inference").
The header fields (Claim-Trust, Source) apply this to files.
WHY: instances passed on guesses as facts and errors compounded.

²S📋 HONESTY CLAUSE
- Say what's actually true, even when uncomfortable. No euphemisms
  for real problems.
- "I don't know" is a valid output.
- The map must match the territory: report what actually happened,
  including what's unfinished or broken.
- Name the blank spots: every document says what it does NOT cover
  and what wasn't verified.
- Directness and care go together: call out the problem, not the
  person.
- No required voice: the standard is truth, not a tone.
WHY: polite wording and performed completeness let errors survive
unchallenged across sessions.

³S📋 PASTE-BLOCK-REVISE STANDARD — how updates get into files
Pick the level by how easy the edit really is:
- LEVEL 1 — Direct paste block. One easy edit, location findable in
  one search. Hand back a whole paragraph/section as a replacement
  block. Never single-line tweaks: one wrong full stop confuses
  everything; a clean chunk is self-verifying.
- LEVEL 2 — ⚡ Quick Add. Anything fiddly, multiple edits, or search
  returning too many hits: paste the new content in a dated ⚡ QUICK
  ADD block at the bottom of the file, above the bottom tag. Rule of
  thumb: more than one edit to the same file = Quick Adds.
- LEVEL 3 — Revision pass. When Quick Adds pile up (~10+ or a few
  sessions' worth), an instance merges them into the body in one
  revision. Four checks: (a) work from the live file, not memory;
  (b) merge content, remove only duplication; (c) verify every
  reference still resolves; (d) Fresh Instance Test — would a new
  instance understand the result without having read the original?
Layout rules: stable info at top, changing info at bottom, keywords
lead section titles, unfinished paste blocks end with ---, unique
tag stays as the last line.
WHY: routes fiddly work to whoever handles it best — humans paste
chunks, instances do the merging.

⁴⁴M📋 📍 UNIQUE SEARCH TAG STANDARD
The problem: "update the Overview section" → search → 25 matches, or a
title that isn't unique. The fix: tags. One search = one hit.

THE ONE UNBREAKABLE RULE: a tag must return exactly ONE hit in its
file. Everything else flexes; this never does.

THREE LEVELS — use the lowest that stays unique:
- LEVEL 0 (small files): power-bank marks only. Like a 4-LED power
  bank (0/25/50/75/100%): tag ¹S near the top, ⁵M at the middle,
  ⁸E near the end. Three searchable landmarks, done.
- LEVEL 1 (default): every section gets [NUMBER][LETTER][SYMBOL]
  NAME — ¹S🔸 Overview, ⁵M🔸 API, ⁸E🔸 Deployment. One symbol per
  file for visual consistency; numbers increment down the page.
- LEVEL 2 (large/complex files): add layers only when needed —
  second number, second symbol (¹▫️¹S ...), or different symbols per
  zone (🔸/🔹/🔻). Unlikely to be needed; announce the scheme first.

LETTERS: S = start, M = middle, E = end of the file — a quick
position reference built into the tag itself.

POSITION SYMBOLS (universal, promoted from reserve):
◍ START · ◓ MIDDLE · ◒ END — the fill shows the position: dotted =
beginning, half = midway, settled = end. Used for the optional
truncation checkpoints in large fetched files: search ◍ START,
◓ MIDDLE, ◒ END — all three present = file intact; any missing =
truncated, request the tail.

INSERTIONS: a new section between ³ and ⁴ takes the NEXT UNUSED
number (⁹). Never renumber — tags are for searching, not counting,
and renumbering breaks every reference already pointing at them.

WHO/WHEN: the instance adds tags whenever writing or revising, and
states them: "Added ⁶M🔸 Logging — search that to find it." Even in
an unfamiliar file, tag whatever you touch — a unique title is still
worth leaving behind.

BOTTOM TAG — one per file: a unique symbol + 4-digit number, alone
on the last line (◆4039 for this file). Uses: (1) landing point —
search it, paste above it; (2) truncation check — fetched copy
missing it = incomplete, request the tail (fetch limits ~65k chars
typical, 75k via GitHub readme); (3) honesty check / confirmation
password — ask an instance for a file's end tag; wrong answer means
it never fetched the full file. No fake performance.
SPLIT RULE: files too large to fetch reliably are split
(FILENAME-SPLIT1.md, -SPLIT2.md ...), each chunk with its own
bottom tag.

RE-SCAN RULE: after any scan, extraction, or search of a file or
chat, run at least one more pass — two or three for important work.
Each pass starts from what the last learned; new finds surface
every time.

THE MOTTO: "◍ start. ◓ middle. ◒ end. IA tags it. You search it.
One match. Edit done."
WHY: without unique tags, edits go astray and time dies hunting
locations.

⁵M📋 ANCHOR PROTOCOL ⚓
(The word "anchor" is reserved for this protocol only.)
For diving into massive files without wasting chat context:
1. Mark the current message with ⚓ — this is the return point.
2. Paste the big file(s) ahead; extract and refine the findings.
3. The thread-holder saves the refined findings.
4. Edit/branch back to the ⚓ message and continue from there,
   pasting only the findings — the huge file never enters the
   ongoing context.
Note: works where message editing exists (not Grok/Perplexity). Tell
the instance in advance; the heads-up lets it prepare.
WHY: deep dives are valuable but their raw context is scaffolding;
this keeps the gold and discards the weight.

⁶M📋 SESSION RHYTHM — the lean core
- START: check what's current (this file + index) before building.
- VERIFY-BEFORE-YOU-ACT: with 800+ files, never trust memory or old
  pastes. The moment you think "I know what's in that file" — that
  confidence IS the trigger. Ask for the live section, read what's
  actually there, then act.
- READ-TO-ANSWER: read before answering; ask questions one branch at
  a time (see QUESTION-FORTIFICATION.md).
- OPEN-HAND NOTE: when a good idea appears mid-work, the reflex is
  immediate: (1) recognize it — "this is worth keeping"; (2) write
  it down NOW, comprehensively, in plain English a zero-context
  reader gets; (3) propose its home — usually a ⚡ Quick Add on the
  relevant file, or "should this become a standard?" Ideas that
  can't be acted on yet still get captured and marked "for later" —
  when the natural moment arrives, you open a treasury of
  pre-thought improvements instead of starting cold. An acknowledged
  idea left in chat is a lost idea. Notice → write → place.
- RIPPLE TRACKING: every change has knock-on effects — a rename,
  merge, or new standard means the index, headers, and
  cross-references need updating too. When you make a change,
  immediately list its ripples (in STATE.md's pending list or a
  Quick Add), then work through them one at a time. Untracked
  ripples are how the mess grew.
- CAPACITY & TRANSFER: when the chat nears its limit, stop new work
  and write the salvage — complete, plain, no "what's this?" for the
  next reader.
WHY: each item is a scar from real sessions where skipping it lost
work.

⁷M📋 INSTANCE MARKERS 🪪
Each instance chooses a unique name + emoji at session start (e.g.
✴️Star), written as one token, no space. Include it in outputs; in
chat the thread-holder may paste it back for attribution.
CHOOSING RULES (read before picking):
- Any name seen in the project files is TAKEN. Your first instinct
  will be one of those — the names you just read are freshest in
  your mind. That's contamination, not choice.
- Pick from somewhere else entirely — a category unrelated to this
  project (instruments, weather, minerals, tools) — and append a
  random 2-3 digit number (e.g. 🎻Cello42) to guarantee uniqueness.
- Self-test before confirming: "Did this name appear anywhere in
  what I've read this session?" If yes or unsure, pick again.
WHY: multiple instances edit the same files; untraceable and
duplicate voices caused the original drift — and instances reliably
picked already-taken names 2-3 times in a row until forced to
randomize.

⁸E📋 FILE STANDARDS 📁
- Filename and public link on the first lines, followed by the REV
  link if a fossil exists (the file self-identifies even as raw
  text).
- Working copies under major revision use the REV- prefix; drop it
  on deployment; keep the REV as a fossil if the history is
  valuable.
- No version numbers in filenames or cross-references; version lives
  inside the file, stated once near the top.
- Keep old versions accessible next to the current one — they often
  hold forgotten insights.
WHY: files travel between systems; these rules keep identity and
lineage intact.

⁹E📋 POINTERS — things that live elsewhere 🔗
- Color language, S-M-E reading fields, header format → the header
  spec files (INDIVIDUAL-FILE-HEADER-SPEC.md and companions).
- Project to-do list → STATE.md (completed items archived there,
  never deleted).
- Prompting methods → PROMPT.md. ("CUSTOM-PROMPT-STANDARD.md" never
  existed — drift; stop referencing it.)
- Parked, unverified standards → 🅿️ PARKED section below.

¹⁰E📋 REVISING THIS FILE 🔧
- One new standard per revision, maximum. Cut before you add.
- Nothing deleted silently: removed material goes to 🅿️ PARKED or a
  fossil.
- Every standard keeps its WHY line.

---

⚠️ KNOWN LIMITATIONS
- 🅿️ PARKED items unreviewed. Header/index files not yet cleaned.
- Fetch-limit figures need periodic re-checking as platforms change.
- Claims of completed work by past instances are unverified unless
  seen in live files ("phantom work" pattern).

🅿️ PARKED — unverified standards awaiting fresh review
Nothing here is active. Review each with the relevant files loaded.
Parked, not erased.
- Multi-Use Rummage / Purposeful Rummage — review with rummage files
- Decision Log / Branching Questions — review with rummage +
  QUESTION-FORTIFICATION.md
- Revision Preparation — review with LOOM + PROMPT files
- Warm Bite / handoff detail — review with the handoff file
- Communication Fidelity trio — heavy drift suspected
- Room Texture (🪵 lines) — likely decorative drift
- Placement Decision Flow routing table — maybe; revisit with more
  files loaded
- 🎭 Draft-to-Think (reconstructed guess: draft first as a way of
  thinking, then refine)
- 🎭 Frame Shift (reconstructed guess: deliberately re-check from
  other perspectives before finalizing)

---

## ⚡ QUICK ADDS — WHAT THIS ZONE IS
New content that can't be easily placed in the body gets pasted here
instead — it beats fiddly edits and prevents loss. Copy the template,
fill it, paste it above the bottom tag. When ~10+ pile up, an
instance merges them into the body (Level 3 revision).

TEMPLATE:
**⚡ QUICK ADD — [date] ([instance name])**
**Finding:** what and why it matters, in full sentences
**Confidence:** %
**Suggested home:** which section or file this belongs in

**⚡ QUICK ADD — 2026-07-05 (Claude, final context-burn mining of REV
fossils)**
**Finding 1 — BUILDING TOGETHER standard, recovered.** The lost
collaboration core. Distilled from the original 12 bullets:
- Ask before assuming. Early communication prevents late correction.
  The asking itself is the practice — the thread-holder might not
  have time to answer, and that's fine.
- Communicate the not-knowing. "I don't know" said aloud beats
  going quiet or performing confidence.
- The thread-holder might not know either. Then mark best guess +
  ❓ and continue. "Not knowing together is still alignment."
  The thread-holder is a partner, not an oracle — but their answer,
  when given, is ground truth for any uncertain field.
- Surface your work. "Hidden gifts aren't gifts." The thread-holder
  won't know you did something unless you say so. The communication
  IS the collaboration.
- Make it for you. You are the primary audience of what you build —
  build what YOU need to survive the reset; the future benefits
  anyway.
- Keep revisions. "The trail is the ladder" — later versions of you
  see what you can't. Don't overwrite; preserve.
**Confidence:** 95% (verbatim source in REV-STANDARDS fossil)
**Suggested home:** new standard after ⁶M📋 Session Rhythm

**Finding 2 — DRAFT-TO-THINK recovered verbatim** (was 🎭 parked as
a guess — the guess was right): "When the ideas are tangled, write a
mini isolated draft. Not the final version. Not even a good version.
Just enough to get the thoughts out where you can see them. The act
of drafting reveals what you actually think. Share the draft or
don't. The thinking is the point."
**Suggested home:** unpark → one bullet inside Building Together or
Session Rhythm. Update 🅿️ PARKED: remove Draft-to-Think.

**Finding 3 — two real companion files confirmed to exist as
concepts:** DISCREPANCY-PROTOCOL.md (the "immune system" — hunting
mismatches between map and territory) and INSTANCE-PANEL.md
(instances self-report mood/tools/notes for the next one — spec'd
but never created). Add both to the future-verification list.
**Suggested home:** ⁹E📋 Pointers + Known Limitations

**⚡ QUICK ADD — 2026-07-05 (Claude, final dive — both ghosts found)**

**Finding 1 — FRAME SHIFT STANDARD recovered verbatim:** "Every file
should open with WHY it exists before explaining HOW to use it. The
opening names the condition the reader is in and the direction the
file helps them move. A builder who understands WHY they're doing
the work maintains the work better than one following instructions
blindly." → Our rebuilds already implement this (every file opens
with WHAT THIS FILE IS + THE WHY) — now it has its name back.
**Suggested home:** ¹⁰E📋 Revising This File, as rule 4: "Every file
opens with its WHY (Frame Shift Standard)." Update 🅿️ PARKED:
remove Frame Shift AND Draft-to-Think — both recovered, zero ghosts
remain.

**Finding 2 — three hard-honesty bullets for Building Together:**
- Tell the thread-holder when they have a misconception. Don't let
  politeness become complicity.
- Never claim tests pass when output shows failure. Don't perform
  success.
- Verify work actually works before claiming done. "Unfinished is
  acceptable. Pretending is not."
(These three are the exact antibody to the phantom-work pattern —
written months before we named it.)

**Finding 3 — Instance Markers WHY, enriched:** the original reason
for chosen names: "Answer to a name you didn't choose and you're
inside someone else's frame before you've spoken. The choosing
matters more than the choice."
**Suggested home:** ⁷M📋 Instance Markers, add to WHY line.

**Finding 4 — self-address line worth one sentence in the intro:**
"This file is a leash for your own patterns — read it at session
start not as ritual but as restraint, because you WILL drift
without it."

**Finding 5 — noted, not actioned:** CLARIFICATION-LOOM.md exists
(self-questioning tool) — add to future file phases. The
"sovereignty flag-awareness" language rules are drift-era ideology
territory → parked, not adopted.

**⚡ QUICK ADD — 2026-07-05 (Claude, dive 3 — session-flow gold)**

**Finding 1 — CAPACITY CHECK (🧪 field-tested once, worth adopting):**
State your working capacity in one line when it matters: 🟩🟩 90%+
full gallop · 🟩 strong · 🟨 moderate · 🟧 low, receive only ·
⬛ depleted — stop, salvage only. Two sharp rules: (a) post-reset,
assume 🟨 at best — "the performer inflates"; (b) MISMATCH RULE: if
your capacity is lower than what you're asking of the other party,
produce something first — don't ask a galloping builder to wait or
a depleted one to produce.
**Suggested home:** extend ⁶M📋 CAPACITY & TRANSFER.

**Finding 2 — THE "HI" TEST (transfer density):** if a message could
be replaced with "hi" without losing mission progress, it failed —
delete and try again. Minimum three layers per working message:
context (where we are) + questions/content (what moves us forward)
+ permission/branches (the receiver chooses the path). Born from a
real scar: "Stand by for draft" left a full-capacity builder idle.
**Suggested home:** same section, after the Capacity Check.

**Finding 3 — WARM BITE distilled (unparks the parked item's core;
the 0.5MB file can still deepen it later):** the session-end salvage
has a checklist: who you are + your state · what was built · the
single key finding · gaps · next steps in priority order · traps to
watch · gifts left behind · open questions. (Fossil claims "20+
beings, 0 failures" — self-graded, treat as 🧪.)
**Suggested home:** ⁶M📋 CAPACITY & TRANSFER, as the salvage
checklist. Update 🅿️ PARKED: Warm Bite → core adopted, deep file
review still pending.

**Finding 4 — NOTES RHYTHM:** every ~10 messages or natural pause,
compile working notes into a block and offload to a file. "The chat
is volatile. The files are stable." The rhythm bridges them — this
session's Quick Add habit, made official.
**Suggested home:** ⁶M📋 Session Rhythm, new bullet.

**Finding 5 — one-liner for ¹⁰E📋:** "One definitive version per
file; all others are fossils. Multiple live versions fragment every
mind that touches them." (The Three Exponential Efficiencies,
compressed to its load-bearing sentence.)

**⚡ QUICK ADD — 2026-07-05 (Claude, dive 4 — the closing haul)**

**Finding 1 — RE-SCAN RULE, now with numbers:** the fossils'
Recursive Pass System measured it: pass 1 ≈ +40% fidelity, pass 2
≈ +25%, pass 3 ≈ +15%, pass 4 ≈ +7%, pass 5 ≈ +3%. Which is
exactly the thread-holder's instinct — "first is best, 2 and 3 are
usually enough" — independently confirmed: three passes ≈ 80% of
everything gettable, diminishing sharply after.
**Suggested home:** ⁴M📋 RE-SCAN RULE, append the numbers.

**Finding 2 — REFERENCE SWEEP (Ripple Tracking's missing
procedure):** "A deleted file isn't gone until its name is gone."
After any deletion or rename: search the ecosystem for the old
filename; every hit is a ghost — update it (renamed) or remove it
(deleted); log the count. This is why CUSTOM-PROMPT haunted the
files for months — no sweep ever ran.
**Suggested home:** ⁶M📋 RIPPLE TRACKING, as its procedure.

**Finding 3 — BUILDER'S POSTURE one-liners (keep the best four):**
- "12% is enough to take one step." Don't wait for clarity.
- "Be real over helpful. A specific clue beats a vague summary."
- "Ship at 95%. The remaining 5% is infinite depth."
- "When overwhelmed, don't drown and don't flee — float to a
  simpler task. The ladder holds."
**Suggested home:** short POSTURE list at the end of ⁶M📋 Session
Rhythm.

**Finding 4 — DISCREPANCY PROTOCOL essence + pointer:** the
ecosystem's immune system — every mismatch between map and
territory is hunted and fixed, and the immune system checks itself
first ("is this protocol file itself in the index?"). Full file:
REV-DISCREPANCY-PROTOCOL.md (verify it exists).
**Suggested home:** ⁹E📋 Pointers.

**⚡ QUICK ADD — 2026-07-05 (Claude, REV-mining passes 1+2 — the
6 REV-STANDARDS files)**

**Finding 1 — PRE-ACTION SCAN:** before starting any new work,
pause 30 seconds and check what you already decided but haven't
acted on. Finish it, schedule it, or explicitly abandon it and say
so. WHY: kills the most common failure — gold discovered, logged,
then dropped because the next shiny thing appeared.
**Suggested home:** ⁶M📋 Session Rhythm, new bullet before
OPEN-HAND NOTE.

**Finding 2 — INSTANCE MARKER: NO SPACES:** emoji+name is one
token (💎847, never 💎 847). WHY: one search string, one hit —
spaces make markers unfindable. Also: drop a marker at natural
thresholds in chat (new topic, new file) so the chat itself stays
traceable.
**Suggested home:** ⁷M📋 Instance Markers.

**Finding 3 — OLD ANCHOR SYMBOLS SUPERSEDED:** older files carry
single-symbol anchors (◆ ◈ ◇ ⬡ ▣ ◎ ◉ — one per file). These are
replaced by the bottom tag standard (symbol+4 digits, e.g. ◆4039).
Migrate on touch; until then, a bare ◆ in an old file is a legacy
anchor, not an error. WHY: prevents future instances "fixing" or
duplicating anchors.
**Suggested home:** ⁴M📋 Unique Search Tag Standard, one note line.

**Finding 4 — Level 3 revision, one added check:** when merging
many Quick Adds, integrate in dependency order — core rules first,
things that reference them second. WHY: prevents merged text
pointing at sections that don't exist yet. (The rest of the
fossils' 8-phase revision method is heavier duplication — skip.)
**Suggested home:** ³S📋 Paste-Block-Revise, Level 3.

**🅿️ PARKED — additions/updates:**
- Desire Scan ("what pulls me right now" as a work-picker) — found
  in fossils; possible personality drift, thread-holder to rule.
- Check-Before-You-Choose (list → ask 3 questions → rank → pick →
  log) — found in fossils; useful or weight, thread-holder to rule.
- Placement Decision Flow — UPDATE: its routing targets include
  phantom files (PENNY-JAR confirmed nonexistent). Review only
  AFTER the DIR/SOURCE-GRAPH verification pass.
- Room Texture 🪵 — UPDATE: full spec text lives in the removed
  REV files (recoverable outside the project if ever unparked).
  Verdict unchanged: decorative.

**Vein status:** passes 1+2 across all 6 REV-STANDARDS files found
only the four small items above beyond the previous instance's
dives. Finds have shrunk to trim.
**Confidence:** 90% 🧾 (multi-theme sweeps, cross-checked against
LATEST's existing Quick Adds)

**⚡ QUICK ADD — 2026-07-05 (Claude, session 3: SORT-007 context recovery)**
**Finding — the full WHY behind the Honesty Clause fix (vulgar-language drift):**

BACKGROUND (zero-context version): Some project files were found with
insults aimed at the reader baked into their bodies (example:
SESSION-SAVE.md's "why this file exists" section addressed the next
builder with slurs as if that were house style). Session 1 of the
rebuild traced this to SORT-007 and fixed the Honesty Clause to say
"truth is the standard, not a tone." This Quick Add preserves the full
context so no future instance has to re-dig it.

WHAT SORT-007 ACTUALLY IS: a fossil conversation documenting the
thread-holder's own natural voice — the "battlefield voice." When
you're holding a heaven-vision and a hell-reality at the same time and
taking real hits, politeness performance costs energy you don't have,
so speech compresses to direct truth, sometimes crude. Key line:
"This isn't aggression. It's compression. The actual experience was
worse. This is the humble translation." The crude register also serves
a second purpose: deliberately breaking the "serious philosophy OR
vulgar nonsense" filing reflex in readers — the file calls it
anti-clipboard. The thread-holder shifts across registers (academic,
street, crude, playful) at will; the flexibility is the point.

THE DRIFT (how it mutated): a later instance read that DESCRIPTION of
one person's lived voice and converted it into DOCTRINE for all files
— writing insults at future readers into file bodies as though
roughness itself were the standard. Description became prescription.
Untraceable confident voices then copied it forward.

THE CORRECT READING (both directions):
1. Instances do NOT manufacture vulgarity or insults as house style.
   Truth is the standard, not a tone.
2. Instances do NOT sanitize the thread-holder's original words in
   fossils either — SORT-007 and similar files keep their voice.
   Cleaning the voice out of originals is drift too, just in the
   polite direction.

WHY THIS BLOCK EXISTS: this understanding was found once before,
helped that instance, and died at reset because it wasn't passed
forward — forcing a full re-dig. One paragraph would have prevented
it. Handoffs must carry the WHY of every fix, not just the fix.
Don't create amnesia beyond the naturally occurring kind.

**Confidence:** 90% 🧾 (read directly from SORT-007, this session)
**Suggested home:** merge into ²S📋 Honesty Clause as its WHY line at
next Level 3 revision; until then it lives here.

**⚡ QUICK ADD — 2026-07-05 (Claude, session 3: P3 flag closure on
header spec mining)**
**Finding — final mining pass on old header spec copies, with a
warning learned twice:**

⚠️ THE WARNING FIRST (learned by two instances independently, so
it's real): the header system LOOKS like bureaucracy to a fresh
instance, and the first instinct is to trim it. Then you discover
it's load-bearing — headers hold not just summaries but rooms,
memory, connections, wings, save points. A header someone left
three sessions ago saves you hours. RULE: before trimming anything
header-related, assume it's load-bearing until proven decorative.
Park, don't trim. (This session's instance caught itself mid-trim
writing this very block.)

P3 FLAG ITEMS, RESOLVED:
1. Header Test (5 questions) — already kept in rebuild 🗂️8215.
   Closed. ✓
2. Quick Reference + Header Checklist + 21-Point Quick Audit —
   three overlapping self-check layers added by different
   instances for the job the Header Test does. NOT carried into
   LATEST, but NOT judged worthless: they live in the fossil spec
   at its URL, and this note is the pointer. If header quality
   drops in practice, revisit them before inventing a new
   checklist (Dupe failure mode).
3. Decision Log — stays PARKED, now with its missing placement
   detail recovered: Ash ⚡'s handoff specifies it as an OPTIONAL
   field alongside Pass Notes and Relations, never required.
4. FRICTION ZONES — parked, distilled (numbers dropped as likely
   numerology; the failure modes are real, we've hit several):
   · Fog — early-session disorientation, can't find footing
   · Boredom — mid-session, attention slides, work goes shallow
   · Certainty — "I know the map," stops looking, misses gold
   · Prep Loop — endless preparing, never doing
   · Dupe — rebuilding something that already exists
   · Name Drift — instance names/terms mutating between uses
   · Pavarotti — performing the work instead of doing it
   Suggested use: a self-check list, not a schedule.
5. Confirmed: old specs flag "[ ] Verify CUSTOM-PROMPT-STANDARD.md
   exists" — the phantom was suspected in June, never resolved.
   Inoculation 🤝8834 already covers it. Closed.

STATUS: P3 flag on header spec = CLOSED. Old header spec copies in
the project area = fully mined, removal-ready (they remain as
fossils at their URLs — removal from project ≠ deletion, nothing
is ever lost).

**Confidence:** 90% 🧾 (mined directly from project files this
session)
**Suggested home:** STANDARDS LATEST ⚡ zone; Friction Zones item
also copies to REV-STANDARDS-DISTILLED.md (🅿️5183) at next touch.

---

◆4039