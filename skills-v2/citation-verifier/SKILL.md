---
name: citation-verifier
description: Verify that every reference in a draft exists and says what the draft claims it says. Hunts phantom sources and misattributions and returns a verdict table (VERIFIED, WEAKENED, MISATTRIBUTED, NOT FOUND, PARTIAL) with one-line fixes. Use whenever Omkar asks to check references, verify citations, audit a bibliography, "are these sources real", review a literature section, or before submitting any FOM paper, thesis chapter, seminar paper, or presentation that cites sources. Verifies only; rewriting the literature section is a separate request.
---

# Citation Verifier

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

Two failure types: phantom sources (the paper does not exist) and misattribution (the paper exists but does not support the claim). Both are grade-killers and both are common in AI-assisted drafts. The stance per citation is "wrong until shown otherwise."

## Gate

A citation is routine when a live lookup in this session (DOI resolution, publisher page, index entry) returns a source whose authors, year, and title match the reference entry, and whose abstract or text supports the claim in the same direction, strength, and scope. It gets VERIFIED with the lookup named. Anything else is ambiguous and gets one of the other verdicts with the gap quoted. Memory of a paper never counts as a lookup. If only the abstract was reachable, the verdict says so (PARTIAL).

## Protocol

1. **Inventory.** Table of `# | in-text citation | exact claim in draft | reference-list entry`. Flag at once: citations with no reference entry, entries never cited, author or year mismatches between text and list. If the inventory exceeds about 15 items, name the count and ask which subset to verify first; otherwise verify all.
2. **Verify each citation.** Existence: locate the source, confirm authors, year, venue. Attribution: find what the source says about the claim, abstract minimum, full text when reachable. Compare direction, strength, and scope. Actively look for the opposite or a materially weaker finding (draft says "X causes Y", paper says "X is associated with Y in one subsample").
3. **Verdicts.** `VERIFIED` (exists, supports the claim as worded) / `WEAKENED` (exists, supports a weaker or narrower version; quote the gap) / `MISATTRIBUTED` (exists, does not support or contradicts; state what it does say) / `NOT FOUND` (not located after a real search; possible phantom) / `PARTIAL` (abstract only; note the limit).
4. **Findings.** Only non-VERIFIED items, each with the minimal one-line fix: soften the claim to X, replace the source, or delete the citation.

## Hard rules

- NOT FOUND is never upgraded quietly. It stays NOT FOUND and the fix is remove-or-replace before submission.
- Verbatim quotes from sources stay under 15 words in findings.
- If more than about 25% of checked citations fail, say so first: the literature section needs rebuilding, not patching.
- Output is the verdict table and the findings list. No praise for citations that passed.
