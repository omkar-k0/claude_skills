---
name: ship-with-eval
description: Definition of done for Omkar's portfolio projects. A project is not done until it has a labelled eval set, a metrics table with the share auto-handled and the accuracy at each confidence band, and those numbers in the README. Blocks any portfolio, CV, or LinkedIn claim that has no eval numbers behind it. Use whenever he says a project is done, shipped, live, or ready, asks to write it up for a CV, README, portfolio page or LinkedIn, mentions eval, labels, metrics table, accuracy by confidence band, or names the Guidance Reconciliation Engine, ContractTracker, or Werkbank. Also use when he wants to build or score an eval set.
---

# Ship With Eval

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

His projects are confidence-gated systems: a rule layer handles routine cases, an LLM judges the ambiguous rest, every decision carries a confidence score. The only honest description of such a system is how much it auto-handles and how accurate it is at each confidence band. "Live on Vercel" is a deployment fact, not a result. Read `references/projects.md` for the current status of each project.

## Gate

A project claim is routine when a metrics table exists in the project repo, at a file path named in the response, and the number being claimed is in it. It may be written into the README, a CV bullet, a LinkedIn line, or a portfolio page, citing that file. A claim with no table behind it is blocked: the deliverable says "eval pending" in its place, and the response names the smallest eval that would unblock it. "Eval after shipping" is not a status; the eval is part of shipping.

## Definition of done

1. **Labelled eval set.** Hand-labelled, with the labelling protocol written down (who labelled, blind or not, how disagreements were resolved) and a size stated. Size is a fact, not a target.
2. **Metrics table.** At minimum:

   | confidence band | share of cases | auto-handled | accuracy in band | n |
   |---|---|---|---|---|

   plus the overall share auto-handled and the accuracy of the auto-handled slice. Bands are the system's own gate thresholds.
3. **README numbers.** The table, or its two headline numbers with a link to the table, in the README, dated, with the eval set size.

Missing any of the three means the project is "shipped, eval pending", and that phrase is what any write-up says.

## Building an eval when none exists

Propose the smallest eval that produces a real table: the number of labelled cases, where they come from, who labels, and the stratification across confidence bands so every band has an n. Estimate the labelling time. Do not generate labels; labels come from him or a named labeller.

## Hard rules

- Numbers in any write-up trace to a file in the repo. A number in chat only is unverifiable and does not ship.
- Werkbank's numbers (reports/eval.md) are the format every other project matches.
