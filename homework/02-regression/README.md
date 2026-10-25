# Homework 2 - Machine Learning for Regression

Solution: [homework.ipynb](homework.ipynb) · Task: [homework.md](homework.md)

## Answers

| Question | Answer |
|---|---|
| EDA. Long tail? | No, `fuel_efficiency_mpg` is roughly symmetric (mean 30.0, median 30.0) |
| Q1. Column with missing values | `horsepower` |
| Q2. Median of `horsepower` | 254 |
| Q3. Fill with 0 or mean | With mean (RMSE 2.202 vs 2.205) |
| Q4. Best `r` | 0 |
| Q5. Std of RMSE over seeds | 0.029 |
| Q6. Test RMSE (seed 9, `r=0.001`) | 2.236 |

## How to run

```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook homework.ipynb
```

## Notes

- Linear regression is implemented with NumPy (normal equation, bias column, optional
  regularization `r`), as in the lessons.
- The mean used for Q3 is computed on the training set only.
- The 60/20/20 split is wrapped in a `split(df, seed)` function so Q5 and Q6 can reuse it
  without modifying `df`.

## What I learned

<!-- TODO: write a few lines in my own words -->
