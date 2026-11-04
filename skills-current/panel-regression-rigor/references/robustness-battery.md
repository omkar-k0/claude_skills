# Robustness battery menu

Phase 1 selects from this menu into the battery contract, each with a pass criterion stated in advance (typical default: headline coefficient keeps sign and stays within ±50% of magnitude, or remains significant at the original level; set explicitly per project).

## Standard error stress
- **Alternative clustering:** re-estimate with clustering at the other plausible level (time instead of entity, or two-way). Report SE ratio.
- **Driscoll-Kraay / robust variants** where cross-sectional dependence is plausible.

## Sample stress
- **Winsorization:** 1% and 5% two-sided on the dependent variable and key regressor; compare.
- **Leave-one-out by entity:** drop each entity once (feasible at DAX-scale N); flag any single entity that flips the result.
- **Subperiod split:** halves of the time window (and around known regime breaks, e.g. rate-cycle shifts); report both coefficients.
- **Balanced-panel-only** re-run if the panel is unbalanced.

## Specification stress
- **Estimator swap:** FE ↔ RE (with Hausman context), pooled OLS as the naive benchmark, reported for transparency.
- **Fixed-effects escalation:** add time FE if the main spec has only entity FE (or vice versa); this is often the strongest alternative spec for the adversarial re-estimation.
- **Control set perturbation:** drop each control one at a time; a headline result that depends on one specific control is flagged.
- **Lag structure:** lag the key regressor one period to reduce simultaneity; report.

## Measurement stress
- **Alternative variable definitions:** e.g., alternative spread measure, alternative ESG change definition (any-change vs threshold-change), as available in the actual data.
- **Standardized coefficients** re-run for magnitude sanity.

## Reporting format per check
`<check name> | stresses: <what> | criterion: <pre-stated> | result: <numbers> | PASS/FAIL`
