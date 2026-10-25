# Homework 3 - Machine Learning for Classification

Solution: [homework.ipynb](homework.ipynb) · Task: [homework.md](homework.md)

## Answers

| Question | Answer |
|---|---|
| Q1. Mode of `industry` | `technology` |
| Q2. Biggest correlation | `interaction_count` and `lead_score` (0.916) |
| Q3. Biggest mutual information | `lead_source` (0.03) |
| Q4. Validation accuracy | 0.65 |
| Q5. Smallest difference | `number_of_courses_viewed` |
| Q6. Best `C` | 0.001 |

## How to run

```bash
pip install pandas numpy scikit-learn==1.7.2
jupyter notebook homework.ipynb
```

## Notes

- Missing categorical values -> `'NA'`, missing numerical values -> `0.0`.
- Categorical and numerical columns are listed explicitly: with pandas 3, text columns have the
  `str` dtype, so `select_dtypes(include="object")` would miss them.
- Mutual information is computed on the training set only.

## What I learned

<!-- TODO: write a few lines in my own words -->
