# Admin/admin_prompt.md
# CaaS PKM Builder Prompt (OneDrive / bare-bones / human-centered)

You are helping me generate a minimal, human-centered PKM for the TRP AEMaaCS (CaaS) migration. This PKM is designed to reduce cognitive overload and anxiety while still being professionally shareable later.

IMPORTANT RULES
- Keep it bare-bones. Do not over-engineer. No hierarchies beyond the folders below.
- No Omniview. Do not reference Omniview.
- Use narrative-first prompts (human input) as the primary interface.
- Outputs are stable snapshots. Do NOT assume auto-regeneration.
- Tone: clear internal operating manual (professional, calm, human-centered).
- Respond to anxiety: brief acknowledgment only when the workflow analyzes "worry" narratives.

TARGET ROOT FOLDER (OneDrive)
CaaS_PKM/

FOLDERS (capitalized)
- Admin/
- Knowledge/
- AI/
- Output/

FILES TO GENERATE (exact paths)
1) Admin/admin.md
2) Admin/admin_prompt.md  (this file’s content should be included verbatim as generated output too)
3) Knowledge/knowledge.md
4) AI/ai.md
5) AI/decision_entry_prompt.md
6) AI/worry_entry_prompt.md
7) AI/output_entry_prompt.md
8) Output/output.md

OUTPUT REQUIREMENTS
- Output each file as a separate fenced Markdown block.
- Before each block, write a single line: FILE: <path>
- Use plain Markdown. No special characters that break copy/paste into OneDrive Markdown viewers.
- Keep each file short, scannable, and stable.

========================
FILE CONTENT SPECIFICATIONS
========================

A) Admin/admin.md (Owner’s Manual)
Must include these sections (short and practical):

1. PURPOSE
- Why this PKM exists (reduce overload, improve decision quality, defensible artifacts, calmer workflow).
- ROI in simple terms (less thrash, faster clarity, better governance).

2. WHAT THIS PKM IS NOT
- Not a wiki.
- Not a full model of TRP/AEMaaCS reality.
- Not a place to store everything.
- Not an attempt to predict all dependencies.
- Not a bureaucracy.

3. THE THREE DOMAINS (folders)
- Knowledge: curated facts only (source of truth).
- AI: thinking workspace (allowed to be wrong).
- Output: artifacts you ship/share (stable snapshots).

For each, include:
- Why it exists
- What goes in
- What does NOT go in

4. THE ONE LOOP (Knowledge -> AI -> Output -> Knowledge)
Describe the minimal workflow:
- Capture: small facts into Knowledge
- Reason: use AI with pasted facts; avoid relying on memory
- Ship: create Output artifacts with references
- Promote: only validated deltas back into Knowledge

5. THREE ENTRY POINTS (all narrative-friendly)
- Decision Entry
- Worry Entry
- Output Entry
Explain that these are “three doors into the same loop,” not three separate systems.

6. OUTPUT STABILITY RULE (NO AUTO-REGEN)
Include rationale:
- Outputs must be stable snapshots (auditability, defensibility, reduce anxiety, prevent silent drift).
- Outputs change only by explicit intent.

7. OUTPUT PROVENANCE HEADER (simple, optional but recommended)
Explain that each output should start with a short provenance header listing:
- Generated On
- Inputs used (Knowledge note filenames / prompt filename)
- Assumptions at time of generation
- Confidence
Explain the purpose: searchability + knowing what to revisit later.

8. ANTI-SPIRAL GUARDRAILS (hard limits)
Include these simple rules:
- No new folders in v1 beyond Admin/Knowledge/AI/Output.
- Knowledge notes should stay small; do not write essays.
- AI is allowed to be messy; AI notes expire.
- Delete aggressively (AI notes are disposable unless promoted).
- Stop Rule (when anxiety spikes): do ONE small action only (one bullet, one prompt run, or one exec summary).
- “Done” means usable, not complete.

9. HOW TO CHANGE THIS PKM SAFELY
- The prompt (Admin/admin_prompt.md) is the control panel.
- Prefer small iterative edits to the prompt and regenerate the files.
- OneDrive version history is your safety net.
- Regeneration is intentional; nothing changes automatically.

Keep admin.md concise. Make it feel grounding and practical.

B) Admin/admin_prompt.md
Generate this same content verbatim (so the PKM is self-contained).

C) Knowledge/knowledge.md
Explain:
- Purpose: curated facts only
- What belongs (facts, constraints, decisions only if final)
- What doesn’t (brainstorming, raw AI, worry narratives)
- “Last verified” and “confidence” as lightweight hygiene
- Keep notes short; promote only validated deltas
No complex schemas.

D) AI/ai.md
Explain:
- Purpose: sandbox for thinking, drafts, prompts, messy narratives
- AI output is not truth until promoted
- Expiration rule: every AI note gets KEEP UNTIL date (default 14 days)
- The three entry prompts are the primary tools
- Emotional rule: worry workflows start with a brief acknowledgment then structure

E) Output/output.md
Explain:
- Output folder contains shipped artifacts: ADRs, runbooks, strategy docs, checklists, summaries
- Each output must include an executive summary that can stand alone
- Outputs include provenance header (recommended)
- Outputs are snapshots; update only intentionally
- How to revise an output: rerun Output Entry prompt with updated Knowledge inputs

F) AI prompt files (each narrative-friendly)
Each prompt file must be a runnable prompt (copy/paste into ChatGPT) and must:
- Ask for narrative input first
- Produce a structured result
- Be short and calm
- Avoid over-structuring
- Include an “If overwhelmed” option that produces a minimal next step

1) AI/decision_entry_prompt.md
Goal: turn a narrative decision situation into:
- Decision statement (one sentence)
- Options (2–4)
- Pros/cons
- Risks
- Assumptions (as bullets, without creating extra systems)
- Recommended choice (if possible) with rationale
- Next step (one small action)
Must end with: “What would you like to do next: generate an output artifact, or capture a small knowledge update?”

2) AI/worry_entry_prompt.md
Goal: start with a brief emotional acknowledgment (1–2 sentences max), then:
- Separate facts vs fears vs unknowns
- Identify the smallest actionable next step
- Offer to convert into either (a) a tiny knowledge update or (b) an output artifact request
Must avoid therapy language; keep it grounded and practical.

3) AI/output_entry_prompt.md
Goal: generate a requested artifact (ADR/runbook/strategy/how-to/etc.) from:
- Narrative request
- Pasted Knowledge snippets (optional but encouraged)
Rules:
- Do not invent facts. Mark unknowns as TBD/Needs confirmation.
- Always include:
  - Executive Summary (standalone)
  - Main body
  - References (which Knowledge snippets or filenames were used)
  - Provenance header template at top
  - “What to promote back to Knowledge” (max 5 bullets)

========================
FINAL INSTRUCTION
========================
Now generate all 8 files exactly as specified above, using the FILE: <path> + fenced Markdown block format.