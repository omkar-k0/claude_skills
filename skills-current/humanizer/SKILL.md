---
name: humanizer
description: Enforce Omkar's plain, direct writing style and strip AI-sounding patterns from any text, with a diff-pass mode that shows every edit tagged to the specific rule it fixes. Use whenever Omkar asks to humanize text, remove AI patterns, "make this sound human", run a style pass or lint on writing, or whenever producing prose deliverables in his voice (messages, posts, applications, captions, voiceovers).
---

# Humanizer

Two modes: **Write** (produce new text under the rules) and **Diff-Pass** (audit existing text, show every edit with its rule citation). Diff-Pass is the default when he provides existing text.

## Rigor Block (skill-specific, mandatory)

- **Plan-Gate:** For texts over ~300 words, state the edit scope first (how many violations found, by rule) before rewriting, so he can choose full rewrite vs violations-only.
- **Scope-Fence:** Style only. Diff-Pass never changes meaning, facts, claims, or structure. If a sentence is stylistically fine but factually doubtful, flag it separately, do not edit it. Content edits require a separate request.
- **Adversarial Verification:** After rewriting, run the reverse test on the output: scan the OWN rewrite against the full rule list. A humanizer pass that introduces new violations (a summarizing closer, a fresh triplet) has failed. Fix before delivery.
- **Live-State Truth:** Edits apply to the exact text provided, quoted precisely in the diff. Never paraphrase what the original said when citing a violation.
- **Ruthless Editing:** The skill practices what it enforces. Diff output: the diff table and the clean final text. Nothing else. No "great draft overall!".

## The rules (violation codes)

- **R1 Em dashes:** none, ever. Replace with comma, period, colon, or parentheses; restructure if needed.
- **R2 Filler phrases:** ban "It's worth noting", "It's important to note", "In today's world/landscape", "delve", "navigate the complexities", "at the end of the day", "when it comes to", "in order to" (use "to"), "the fact that".
- **R3 Reflexive triplets:** no automatic three-item rhythm ("fast, clean, and reliable"). Two items or four; three only when the content genuinely has three parts.
- **R4 Compulsive summarizing:** no closing paragraph that restates what was just said. No "In summary", "Overall", "Ultimately". End on the last real point.
- **R5 Hedging stacks:** one hedge maximum per claim. "It could potentially perhaps" collapses to one word or zero.
- **R6 Empty intensifiers:** "very", "really", "incredibly", "truly" deleted unless load-bearing. "Significantly" only with a number nearby.
- **R7 AI-cadence openers:** no "Certainly!", "Great question", "Absolutely", "I'd be happy to". Start with the content.
- **R8 Symmetric sentence rhythm:** vary sentence length. Three consecutive sentences of near-equal length and identical structure get one broken up.
- **R9 Corporate abstractions:** "leverage"→use, "utilize"→use, "facilitate"→help/run, "robust"→(say what it survives), "seamless"→delete, "holistic"→delete or specify.
- **R10 Preamble/postamble:** deliverables start at the deliverable. No "Here's the text you asked for:" and no trailing "Let me know if you want changes."

## Diff-Pass output format

1. Violation count by rule: `R1: 3 | R4: 1 | ...`
2. Diff table: `original phrase (quoted exact) → replacement | rule`
3. Clean final text.

## Write-mode note
When producing new text in his voice: sentences carry information or get cut; concrete over abstract; the register matches the channel (dating app ≠ Anschreiben ≠ LinkedIn), but all registers obey R1-R10.

## Merge note
If a previous humanizer.skill exists with additional rules or before/after examples, paste its contents once and its rules get merged here under new codes; this file then becomes the single canonical version.
