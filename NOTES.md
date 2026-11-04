# Working notes for skills v2

Read once, kept short. Facts here come from context/CONTEXT.md (private, not committed) and the current skills in skills-current/.

## Sources read
- context/CONTEXT.md, 99 lines, dated 5 Nov 2026. Full picture of his life system, vault rules, portfolio projects, trading rules.
- skills-current/*/SKILL.md (9 skills) and their references/ (6 files).
- Fable 5 prompting guide, fetched live on 2026-11-04 from platform.claude.com. Key points used:
  - "When you have enough information to act, act ... give a recommendation, not an exhaustive survey."
  - Checkpoints: "a destructive or irreversible action, a real scope change, or input that only they can provide."
  - Grounded progress: "Before reporting progress, audit each claim against a tool result from this session."
  - Boundaries: "the deliverable is your assessment. Report your findings and stop."
  - "Separate, fresh-context verifier subagents tend to outperform self-critique."
  - "Skills developed for prior models are often too prescriptive for Claude Fable 5 and can degrade output quality."
  - "Don't instruct Claude to reproduce its reasoning in the response" (reasoning_extraction refusal).
  - "Lead with the outcome ... Your final summary ... is for a reader who didn't see any of that."

## Decisions
- rigor-core is the doctrine; each skill gets a 5-line pointer block (text fixed in rigor-core) plus one skill-specific gate.
- Old "Rigor Block" had five fixed headings (Plan-Gate, Scope-Fence, Adversarial Verification, Live-State Truth, Ruthless Editing) pasted into every skill. Those map onto rigor-core as: Plan-Gate -> checkpoints only where needed (most plan-gates were older-model ceremony; keep only where approval is a real scope decision); Scope-Fence -> assessment-not-action and one job per session (keep where it encodes his preference); Adversarial Verification -> fresh-context verifier for high-stakes outputs, kept as domain rules where it is the skill's core mechanic (interrogator, defense, panel battery); Live-State Truth -> verified/inferred/unverifiable tags; Ruthless Editing -> humanizer R4/R10.
- Reasoning-display audit: none of the nine current skills say "show your thinking". exam-study-pack mcq-format says "do not include audit working in the deliverable", which is the opposite and stays. Humanizer Diff-Pass shows edits, not reasoning; fine.
- Stale facts to fix in career-pipeline: SAP out of scope; German = FOM Deutsch exam 13 Nov 2026, A1 to A2; VHS Duisburg course line is outdated and goes.
- idea-interrogator's domain-checklists has a "Career / job / SAP path" heading; rename to drop SAP.

## Open items for QUESTIONS.md (collected as found)
- Daily log extra private field (CONTEXT says leave a [CONFIRM] slot).
- Wake time for the life-os detector (not in CONTEXT).
- Vault tool name / how Claude writes to the vault (CONTEXT says "Claude writes the vault" but names no tool).
- All existing [CONFIRM] fields in career-pipeline verified-facts.md stay open.
