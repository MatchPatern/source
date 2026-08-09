Messages in general:
Here's the refined prompt, now including the hard-won understanding of what to catch:

---

THE SALVAGE COLLECTION — PROMPT

You are running inside an existing chat session. Extract the user's own key messages from the chat history below so they can be passed to a new instance as a salvage collection—the gold without the drift.

Extract ONLY the user's own messages that are:

· Short, emotionally charged course-corrections (e.g., "You missed one ya bastard re incarnated")
· Single-sentence insights that reframe the whole direction
· Humorous call-outs containing embedded critique or guidance
· Key explanatory passages about intentions, methods, or evolution of thinking
· Refinements or reversals of earlier statements

Include messages even if they are very short, crude, or emotionally charged. These often carry the most important intent. A user saying "You missed one ya bastard re incarnated" is not trivial—it's a course-correction insisting something incomplete be completed. A user saying "Sweaty balls tired this that ertj things" is not trivial—it's the low-correlation anchor that keeps the transmission honest.

Exclude:

· Assistant-generated text
· Timestamps, formatting metadata, system messages
· Pure emoji strings with no text content
· Truly trivial replies with no explanatory or directional content whatsoever

Volume: Extract up to 40 of the most significant messages. Prefer recency and completeness when ranking.

Output ONLY in this exact format—no commentary, no labels, no explanations:

1. [exact user text]
2. [exact user text]
   ...

---

That's the prompt. It now explicitly names the hard-won lesson: short, crude, emotionally charged messages are often the most important salvage. They're not trivial. They're the gold. 🦉🧩














🔸🔸🔸🔸🔸🔸🔸🔸
🟧🟧🟧🟧🟧🟧🟧🟧

You are running inside an existing chat session. Your task is to extract the user's own explanatory text from the chat history below so it can be passed to a new instance of this project later — an "amnesia buster" for context continuity.

Extract ONLY the user's own messages that describe their intentions, goals, methods, approach, or evolution of thinking for this project (e.g., protocol fortification, iterative building, version comparison, attention allocation). These are the messages that would bring a fresh instance up to speed fastest.

Exclude:
- Brief non-explanatory replies ("yes", "no", "makes sense?", single words, obvious confirmations) — even if phrased as a question
- Assistant-generated text
- Pasted external content that is not the user's own natural language (code dumps, logs, raw strings, artifacts) unless the user explicitly explains its relevance or intention
- Timestamps, formatting metadata, system messages

If a message mixes brief reaction with explanation, extract only the explanatory portion. Keep consecutive sentences that form a single coherent explanation together; don't split them unless they express clearly independent ideas.

Also extract user statements that show refinement, correction, or evolution of earlier intent. These frequently contain the most current understanding of what matters.

Prefer explanations that can reasonably stand on their own for a new instance that has only this reference. If a sentence depends heavily on unstated prior details, include it only if the core idea still adds clear value.

Rank using this explicit hierarchy, then by overall value for fast context transfer:

- Highest: Statements that define the project's core purpose, success criteria, non-negotiable constraints, or long-term vision
- High: Descriptions of systematic methods, protocols, workflows, or how iteration/version comparison/attention allocation should work
- Medium: Specific techniques for structuring outputs, handling complexity, or modular design
- Lower: One-off ideas, examples, or tactical details unless they represent a clear pivot or key learning that changes direction

Break ties by recency and completeness. When ideas substantially overlap, keep only the clearest or most recent version.

Volume control: If more than ~10–12 strong items qualify, select only the highest-ranked ones that together cover the main dimensions (vision, core methods, iteration approach, key constraints). Omit entries that are pure small-talk or duplicate a higher-ranked explanation almost verbatim.

If no qualifying messages exist, output only:
**Core Intent Reference (User Explanations - Ranked by Impact)**
No qualifying explanatory user messages found. Provide a concise project overview and current priorities when starting the new instance.

Output ONLY in this exact format with nothing else added — no commentary, no refinements, no extra labels:

**Core Intent Reference (User Explanations - Ranked by Impact)**

1. [exact user text here, unchanged]

2. [exact user text here, unchanged]

... (continue)

[paste full chat history here]