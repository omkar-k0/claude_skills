# MCQ bank format and distractor audit

## Format (OMR multi-answer)

Each item:

```
Q<nr>. <stem, one scenario or concept>
A) <statement>
B) <statement>
C) <statement>
D) <statement>
E) <statement>   (optional 5th)
```

- Any subset of A-E may be true, including all or none, matching FOM OMR style.
- Stems are self-contained; no item depends on another item.
- Calculation items include the dataset in the stem, small enough to compute by hand in under 3 minutes.
- Answer key format: `Q<nr>: A, C | A: true because <one line> | B: false because <one line> ...` Every statement gets a justification, not just the true ones.

## Distractor audit (run on every item before delivery)

For each FALSE statement, answer three questions:
1. **Plausibility:** would a student who half-knows the topic pick it? If no one would pick it, replace it. Dead distractors waste the item.
2. **Defensibility attack:** could a fully correct-thinking student argue it is true under any reasonable reading? If yes, the item is broken; rewrite the statement until it is unambiguously false. Ambiguous items are the number one failure mode.
3. **Error-source mapping:** which specific mistake produces this distractor? (Wrong formula, interpolated instead of classical quartile, sign error, confusing Type I/II.) Every distractor should map to a real error. Note the mapping in the answer key justification.

For each TRUE statement: confirm it is true exactly as worded, with no missing condition. "The t-test requires normality" is a broken true statement if the item context is large-sample.

An item passes only when all five statements pass. Report the audit as done; do not include audit working in the deliverable.
