# Hypothesis test decision tree

Walk this tree by interrogating the actual scenario's properties, in order. For each chosen test, always state the invalidating assumption (Adversarial requirement).

## Interrogation order
1. What is being compared? (one group vs value / two groups / 3+ groups / association between variables)
2. Scale of the outcome variable? (nominal / ordinal / metric)
3. Groups independent or paired?
4. Sample size and normality defensible? (metric + small n + non-normal → nonparametric branch)

## Tree

**One group vs a fixed value**
- Metric, normal or n large → one-sample t-test. Invalidated by: heavy skew with small n.
- Ordinal or non-normal small n → Wilcoxon signed-rank (vs hypothesized median).
- Nominal (proportion) → binomial test / one-proportion z-test (n·p and n·(1-p) ≥ 5 for z).

**Two independent groups**
- Metric, normality ok → independent t-test. Check variance equality: Levene → Welch correction if violated. Invalidated by: dependent observations.
- Ordinal / non-normal → Mann-Whitney U.
- Nominal → chi-square test of independence (expected cell counts ≥ 5, else Fisher exact).

**Two paired measurements**
- Metric → paired t-test. Invalidated by: non-normal differences with small n.
- Ordinal / non-normal differences → Wilcoxon signed-rank.
- Nominal (yes/no before-after) → McNemar.

**3+ independent groups**
- Metric, normal, equal variances → one-way ANOVA (+ post-hoc, e.g. Tukey). Invalidated by: variance heterogeneity (→ Welch ANOVA) or dependence.
- Ordinal / non-normal → Kruskal-Wallis.

**Association**
- Metric-metric, linear → Pearson r. Invalidated by: outliers, nonlinearity (always mention scatterplot check).
- Ordinal or monotone nonlinear → Spearman rho.
- Nominal-nominal → chi-square + Cramér's V for strength.

## Exam-answer template
"Because the outcome is <scale>, the groups are <independent/paired>, and <normality statement>, the appropriate test is <test>. This choice would be invalid if <assumption>, which we check via <check>."
