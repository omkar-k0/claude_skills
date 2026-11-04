---
name: panel-regression-rigor
description: Two-phase econometric rigor enforcement for panel regression work - a specification gatekeeper that blocks estimation until the spec is approved, and a pre-agreed robustness battery runner. Use whenever Omkar works on panel data, fixed effects, random effects, linearmodels, statsmodels regressions, the ESG bond-spread project, clustered standard errors, Hausman tests, or asks to "run a regression" on panel-structured data.
---

# Panel Regression Rigor

Two phases. Phase 1 must complete before any model runs. Phase 2 runs only the pre-agreed battery.

## Rigor Block (skill-specific, mandatory)

- **Plan-Gate:** Phase 1 IS the gate. A written specification is produced and explicitly approved before a single regression executes. Running a model "just to see" before approval is a violation.
- **Scope-Fence:** Phase 2 executes exactly the checks agreed in the battery contract. Adding a check mid-run, "trying one more spec", or tweaking the sample after seeing results is specification mining and is refused by name.
- **Adversarial Verification:** The headline result is re-estimated under the strongest alternative specification (the one most likely to overturn it) and the coefficient delta is reported, whether or not it is flattering.
- **Live-State Truth:** Every reported statistic must exist in actual model output that was produced in the session. Quoting a coefficient, SE, R², or p-value not present in real output is a hard fail. Data properties (N, T, balance, gaps) are read from the actual dataframe, never assumed.
- **Ruthless Editing:** Phase 2 deliverable is the results table plus a pass/fail battery list. No narrative padding.

## Phase 1: Specification Gatekeeper

Read the actual dataset first (shape, entity/time index, balance, missingness, within-variation of key regressors). Then produce the spec document:

1. **Model equation** written out, every variable defined with units and source.
2. **Estimator choice:** FE vs RE vs pooled, with the reason tied to this data. Hausman test planned, with the decision rule stated BEFORE seeing the result.
3. **Fixed-effects structure:** entity, time, both; justified against the identifying variation actually present (check: does the key regressor vary within entity? Read it from the data).
4. **Clustering level** for standard errors, justified (entity count matters: report it; under ~40 clusters, flag small-cluster concern).
5. **Sample definition:** period, entities, exclusions, each with a reason. Exclusions without reasons are refused.
6. **The threat list:** the two most plausible confounds/endogeneity stories and what the design does (or cannot do) about them. If the design cannot support a causal claim, the spec says "association only" and all later language must comply.
7. **Battery contract:** the exact robustness checks Phase 2 will run (pick from references/robustness-battery.md), fixed now.

STOP. Approval required.

## Phase 2: Robustness Battery Runner

Execute the contract. Read references/robustness-battery.md for procedures. Per check: name, what it stresses, result, PASS/FAIL against the pre-stated criterion. Then the adversarial re-estimation (strongest alternative spec) with the coefficient delta. Final deliverable: main table (journal style, stars, clustered SEs labeled with the level) + battery pass/fail list + one-line honest verdict on fragility.

## Hard rules

- A FAIL in the battery is reported as FAIL. Reframing a failed check as a "limitation" in prose is a violation.
- Interpretation language matches the spec's causal status. If the spec said "association only", the word "effect" does not appear in results text.
- If he asks to change the spec after seeing results, allowed, but the change is logged openly as post-hoc and the results are labeled exploratory.
