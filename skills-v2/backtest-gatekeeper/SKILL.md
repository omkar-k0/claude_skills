---
name: backtest-gatekeeper
description: Research rigor for Omkar's XAUUSD and multi-market trading work, the trading counterpart of panel-regression-rigor. Phase 1 pre-registers the pass bar, scaling rules, validation design, sealed holdout, and baseline before any test runs; Phase 2 runs it, logs every variant, and reports failed gates as plainly as passed ones. Use whenever he mentions a backtest, sweep-reversal, gate, momentum gate, walk-forward, holdout, profit factor, Brier score, reliability table, cross-market check, scaling by daily range, or wants to change a parameter after seeing results. Demo accounts only, no real money.
---

# Backtest Gatekeeper

> Rigor: see rigor-core. Tag claims verified (source named), inferred, or unverifiable; never guess a `[CONFIRM]`. Act once there is enough information; recommend, do not survey. Report only what a tool result from this session supports. Checkpoint only for irreversible actions, scope changes, or input only Omkar can give. Style: humanizer.

Two phases. Nothing runs before Phase 1 is written down. The house rules are in `references/research-rules.md`; they are not negotiable mid-run.

## Gate

A run is routine when every input (parameters, sample window, markets, scaling constants, thresholds, pass bar) is in the run log before its result is seen; the result is then reported against the pre-registered bar. Any change to any input after a result has been seen opens a new, numbered iteration in the log with the reason stated. A change without a new iteration is not run. A reported statistic exists in output produced in this session or it is not reported.

## Phase 1: Pre-registration

1. **Hypothesis** in one falsifiable sentence, with the reason the edge should exist.
2. **Pass bar**, fixed now. Example: momentum gate must add at least +0.30 profit factor over the baseline.
3. **Baseline:** the best simple gate already in hand (currently the one-feature momentum gate), not plain rules.
4. **Scaling rules** for cross-market runs, fixed once and logged. Example: distances scaled by the instrument's median daily range divided by gold's.
5. **Validation design:** time-ordered walk-forward (never shuffled), embargo between train and test, thresholds chosen inside the training window only, calibration via reliability table and Brier score, luck check on time-shifted labels.
6. **Sealed holdout:** the final test period, named by date, untouched until the model is frozen, then looked at once.
7. **Markets** in the cross-market check, listed. A market that fails is dropped, not tuned.
8. **Expected trade count.** Under about 100 independent trades, say that significance is off the table before running.

Stop for his confirmation; the pre-registration is the contract.

## Phase 2: Run and report

Every variant goes in the run log with all inputs and its iteration number. Report per gate: iteration, inputs, result, bar, PASS or FAIL. Failures are stated as plainly as passes: "M4 iteration 1: no gate passes; momentum gate +0.22 PF, short of the +0.30 bar." The holdout result is reported once, labelled as such, and never re-run.

## Hard rules

- Demo accounts only. No real money. Never touch a partner's accounts.
- A failed market is dropped from the set, not tuned into passing.
- Post-holdout changes are a new study with a new holdout, not an iteration.
