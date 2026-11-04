# Portfolio projects and eval status (from Omkar's notes, 5 Nov 2026)

Status here is the last known state. The session's own file reads override it.

## Guidance Reconciliation Engine (SEC EDGAR guidance vs outcome)
- Live on Vercel since 24 Oct 2026.
- Has: rule layer, confidence gate, LLM adjudicator with quote checks, blind labelling sheet.
- Status: "eval labels pending". No real results yet. Claims allowed: architecture and deployment only.
- [CONFIRM: repo path, target eval set size]

## ContractTracker (MSA obligation extraction)
- Plan: eval set of at least 20 hand-labelled MSAs, "done after V1.1 ships".
- Status: no eval. Claims allowed: what it extracts, not how well.
- [CONFIRM: is V1.1 shipped, repo path]

## Werkbank (furniture order routing)
- reports/eval.md: 40% auto-routed at 96% accuracy on hand-written requests; 83% at 99.7% after 100 simulated corrections.
- Status: done by this skill's definition. The reference format for the other two.
- [CONFIRM: eval set size and labelling protocol are stated in that file]
