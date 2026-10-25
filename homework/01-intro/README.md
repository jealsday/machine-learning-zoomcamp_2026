# Homework 1 - Introduction to Machine Learning

Solution: [homework.ipynb](homework.ipynb) · Task: [homework.md](homework.md)

## Answers

| Question | Answer |
|---|---|
| Q1. Pandas version | 3.0.6 |
| Q2. Records count | 10000 |
| Q3. Fuel types | 3 |
| Q4. Columns with missing values | 2 (`horsepower`, `acceleration`) |
| Q5. Max fuel efficiency (Asia) | 41.2 |
| Q6. Median after filling with the mode | Yes, it decreased (254 -> 252) |
| Q7. Sum of weights | 0.369 |

## How to run

```bash
pip install pandas numpy
jupyter notebook homework.ipynb
```

The data is read from [`../../data/`](../../data/).

## Notes

- Q6: missing values are filled with the **mode** (252), not the median. Filling with the
  median cannot change the median.
- Q7: no bias column, because the task only asks for `vehicle_weight` and `model_year`. The
  notebook also shows a "Q7 bis" with a bias column for comparison (-5913.59, not an option).

## What I learned

<!-- TODO: write a few lines in my own words -->
