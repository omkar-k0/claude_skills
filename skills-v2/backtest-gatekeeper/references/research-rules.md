# Trading research rules (house style, from the XAUUSD project notes, 5 Nov 2026)

- **Pre-register:** write the pass bar and the scaling rules down before running. Example: distances are scaled by the instrument's median daily range divided by gold's, fixed once and logged.
- **Markets that fail get dropped, not tuned.**
- **Validation:**
  - Time-ordered walk-forward, never shuffled.
  - Embargo between train and test.
  - Thresholds chosen inside the training window only.
  - Calibration checked with a reliability table and Brier score.
  - Luck check: rerun on time-shifted labels.
- **Sealed holdout:** a final test period stays untouched until the model is frozen, then gets looked at once.
- **The baseline to beat is the best simple gate,** not plain rules. A new model must beat the existing one-feature momentum gate.
- **Count every variant** in a run log, with all inputs.
- **Report failures plainly.** Example: "M4 iteration 1: no gate passes; momentum gate +0.22 PF, short of the +0.30 bar."
- **Safety:** demo accounts only, no real money, never touch a partner's accounts.

## Known project facts
- Strategy family: sweep-reversal on XAUUSD. Engine: event-driven, config-driven YAML, Dukascopy data, DST-aware session levels, multi-target TP ladder, instrument-agnostic via config.
- [CONFIRM: current run-log file path and format]
- [CONFIRM: the markets in the current cross-market set]
- [CONFIRM: the sealed holdout period for the current study]
