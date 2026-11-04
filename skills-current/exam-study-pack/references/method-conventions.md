# Professor-specific method conventions

These override textbook/software defaults in all solutions and MCQ keys. Extend this file as new conventions are discovered per module.

## QDA (Quantitative Data Analysis)

### Quartiles: classical median-of-halves method (MANDATORY)
The professor requires the classical method, not linear interpolation (which Excel/Python default to).

Procedure:
1. Sort the data ascending.
2. Find the median. Odd n: middle value, EXCLUDED from both halves. Even n: mean of the two middle values; the two middle values stay in their respective halves.
3. Q1 = median of the lower half. Q3 = median of the upper half.
4. IQR = Q3 - Q1.

Worked check example: data 3, 5, 7, 8, 12, 13, 14, 18, 21 (n=9, odd).
- Median = 12 (5th value, excluded).
- Lower half: 3, 5, 7, 8 → Q1 = (5+7)/2 = 6.
- Upper half: 13, 14, 18, 21 → Q3 = (14+18)/2 = 16.
- IQR = 10.

Exam trap to include in materials: numpy/Excel interpolation gives different values on the same data. Any MCQ on quartiles should include the interpolated result as a distractor and the audit must confirm the classical result is the keyed answer.

### General QDA conventions
- Show intermediate rounding only at the final step unless the professor's worked examples round earlier; match the slides.
- When slides and textbook conflict, slides win. Cite the slide number in the solution.

## Template for new modules

## <MODULE NAME>
### <Calculation type>: <professor method>
- Procedure, worked check example, exam trap, source (slide/email/announcement).
