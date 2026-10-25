# Homework 4 - Evaluation Metrics for Classification

Solution: [homework.ipynb](homework.ipynb) · Task: [homework.md](homework.md)

## Answers

| Question | Answer |
|---|---|
| Q1. Highest AUC numerical feature | `lead_score` (0.788) |
| Q2. Validation AUC | 0.732 |
| Q3. Precision/recall intersection | 0.63 |
| Q4. Threshold with max F1 | 0.41 |
| Q5. Std of AUC over 5 folds | 0.007 |
| Q6. Best `C` | 0.001 (mean AUC 0.749) |

## How to run

```bash
pip install pandas numpy matplotlib scikit-learn==1.7.2
jupyter notebook homework.ipynb
```

## Notes

- Q3 ignores thresholds where precision and recall are both 0, then picks the smallest
  `|precision - recall|`.
- Q6 tie-break: best mean, then lowest std, then smallest `C`.

## What I learned

<!-- TODO: write a few lines in my own words -->