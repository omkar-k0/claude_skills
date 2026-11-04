---
name: panel-regression-rigor
description: Two-phase econometric rigor for panel regression work. Phase 1 is a specification gatekeeper that blocks estimation until the written spec is approved; Phase 2 runs only the pre-agreed robustness battery and reports PASS/FAIL per check. Use whenever Omkar works on panel data, fixed effects, random effects, linearmodels, statsmodels regressions, the ESG bond-spread project, clustered standard errors, Hausman tests, Driscoll-Kraay, or says "run a regression" on panel-structured data. Every reported statistic must exist in model output produced in the session.
---

# Panel Regression Rigor

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

Two phases. Phase 1 completes before any model runs. Phase 2 runs exactly the agreed battery. Approving the spec is a real checkpoint: it fixes what counts as a result before any result is seen.

## Gate

A statistic is routine when it appears in model output produced in this session; it is reported with the run it came from. A statistic not in session output does not appear, not even as an illustration. Data properties (N, T, balance, gaps, within-variation of the key regressor) are read from the dataframe, never assumed. Any change to the spec, sample, or battery after a result has been seen is post-hoc: allowed, logged openly as post-hoc, and its results labelled exploratory. "Trying one more spec" without the log entry is specification mining and is refused by name.

## Phase 1: Specification

Read the dataset first (shape, entity and time index, balance, missingness, within-variation). Then the spec:

1. **Model equation** written out, every variable defined with units and source.
2. **Estimator:** FE, RE, or pooled, with the reason tied to this data. Hausman planned, decision rule stated before the result.
3. **Fixed-effects structure:** entity, time, or both, justified against the identifying variation actually present.
4. **Clustering level**, justified; report the cluster count and flag small-cluster concern under about 40.
5. **Sample definition:** period, entities, exclusions, each with a reason. Exclusions without reasons are refused.
6. **Threat list:** the two most plausible confounding or endogeneity stories and what the design does about them. If the design cannot support a causal claim, the spec says "association only" and all later language complies.
7. **Battery contract:** the exact checks Phase 2 runs, picked from `references/robustness-battery.md`, each with its pass criterion.

Stop for approval.

## Phase 2: Battery

Run the contract. Per check: name, what it stresses, criterion, result, PASS or FAIL. Then the adversarial re-estimation: the strongest alternative specification, the one most likely to overturn the headline, with the coefficient delta reported whether or not it flatters. Deliverable: main table (journal style, stars, clustered SEs labelled with the level), the battery PASS/FAIL list, and one honest line on fragility.

## Hard rules

- A FAIL is reported as FAIL. Reframing it as a "limitation" in prose is a violation.
- Interpretation language matches the spec's causal status. Under "association only", the word "effect" does not appear in results text.
