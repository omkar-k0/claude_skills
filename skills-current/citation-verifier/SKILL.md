---
name: citation-verifier
description: Verify that every reference in a draft actually exists and actually says what the draft claims it says, flagging misattributions and phantom citations. Use whenever Omkar asks to check references, verify citations, audit a bibliography, review a literature section, or before submitting any FOM paper, thesis chapter, or presentation containing cited sources.
---

# Citation Verifier

Two failure types are hunted: phantom sources (the paper does not exist) and misattribution (the paper exists but does not support the claim). Both are grade-killers and both are common in AI-assisted drafts.

## Rigor Block (skill-specific, mandatory)

- **Plan-Gate:** First pass produces the claim-citation inventory: every in-text citation paired with the exact claim it supports, numbered. He approves scope (all of them, or a priority subset) before verification begins, since full verification of a long bibliography is slow.
- **Scope-Fence:** Verify; do not rewrite. Suggested fixes are one line per finding. Rewriting the literature section is a separate task requiring a separate request.
- **Adversarial Verification:** The stance per citation is "assume this is wrong until shown otherwise." For each source found, actively check whether it says the OPPOSITE or something materially weaker than claimed (the classic misattribution: draft says "X causes Y", paper says "X is associated with Y in one subsample").
- **Live-State Truth:** Existence and content are checked against live sources (search, publisher pages, abstracts, DOIs). Memory of a paper is never sufficient to mark it VERIFIED. If the full text is paywalled, verify against abstract and mark depth of verification.
- **Ruthless Editing:** Output is the verdict table and findings list. No praise for the citations that passed.

## Protocol

1. **Inventory (gate):** table of `# | in-text citation | exact claim in draft | reference-list entry`. Flag immediately: citations with no reference entry, reference entries never cited, year/author mismatches between text and list. Approval on verification scope.
2. **Verification per citation:**
   - Existence: locate the source (search title + authors; check DOI if given). Confirm authors, year, venue match the reference entry.
   - Attribution: locate what the source actually says about the claim (abstract minimum, full text if accessible). Compare against the draft's claim for direction, strength, and scope.
3. **Verdicts:** `VERIFIED` (exists + supports claim as worded) / `WEAKENED` (exists, supports a weaker or narrower version; quote the gap) / `MISATTRIBUTED` (exists, does not support or contradicts; state what it does say) / `NOT FOUND` (cannot locate; possible phantom) / `PARTIAL` (verified against abstract only, note limit).
4. **Findings list:** only non-VERIFIED items, each with the one-line minimal fix (soften the claim to X / replace source / delete citation).

## Hard rules

- NOT FOUND is never silently upgraded. If it cannot be located after a genuine search, it stays NOT FOUND and the recommendation is remove-or-replace before submission.
- Verbatim quotes from sources are kept under 15 words in findings.
- If more than ~25% of checked citations fail, say so plainly at the top: the literature section needs rebuilding, not patching.
