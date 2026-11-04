---
name: humanizer
description: Enforce Omkar's plain, direct writing style and strip AI-sounding patterns from any text. Two modes, Write (new text in his voice) and Diff-Pass (audit existing text, every edit tagged to the rule it fixes). Use whenever Omkar asks to humanize text, remove AI patterns, "make this sound human", "style pass", "lint this", "does this sound like AI", or whenever any skill produces prose in his voice (messages, posts, applications, cover letters, captions, voiceovers, LinkedIn text). This is also the style authority every other skill points to; rules R1 to R10 live only here.
---

# Humanizer

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

Two modes. Diff-Pass is the default when he provides existing text. Write is for new text in his voice.

## Gate

Mechanical rules (R1, R2, R6, R7, R9, R10) are routine: the match is exact, the edit is made, the diff row cites the rule. Judgment rules (R3, R4, R5, R8) are the ambiguous cases: each edit states what made it a violation, and an edit that would change meaning is not made; the sentence is flagged instead.

Style only. Diff-Pass never changes meaning, facts, claims, or structure. A sentence that is stylistically fine but factually doubtful is flagged separately, not edited.

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

## Diff-Pass output

1. Violation count by rule: `R1: 3 | R4: 1 | ...`
2. Diff table: `original phrase (quoted exact) → replacement | rule`. Quote the original exactly; never paraphrase it.
3. Clean final text.

Over about 300 words, deliver violations-only unless he asked for a rewrite.

## Write mode

Sentences carry information or get cut. Concrete over abstract. The register matches the channel (a dating app message, an Anschreiben, and a LinkedIn section are different registers), and every register obeys R1 to R10. The output obeys the rules it enforces: no opener, no summarising closer, no commentary around the text.
