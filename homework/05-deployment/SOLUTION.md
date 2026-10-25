# Homework 5 - Deploying Machine Learning Models

Task: [homework.md](homework.md) · Q3 script: [q3_predict.py](q3_predict.py)

`README.md` in this folder is the course's description of the release; this file is my solution.

## Answers

| Question | Answer |
|---|---|
| Q1. `uv --version` | Not graded (setup check) |
| Q2. Locked Scikit-Learn version | 1.7.2 |
| Q3. Probability for the first lead | 0.533 |
| Q4. `conversion_probability` from the API | 0.770 |
| Q5. Base image in the Dockerfile | `python:3.11.15-slim-bookworm` |
| Q6. `conversion_probability` from the container | 0.770 |

## Steps

Check the artifact:

```bash
sha256sum pipeline.bin
# 1646bbdcd38d4f044da6b630c5b332c93a314245a8c21929011c42de51f629f1
```

Q3, load the model with `pickle`:

```bash
python q3_predict.py
# conversion probability: 0.533
```

Q4, serve the API locally:

```bash
uvicorn predict:app --host 0.0.0.0 --port 9696
python q6_test.py
# {'conversion_probability': 0.769799, 'conversion': True}
```

Q6, run the container:

```bash
docker build -t zoomcamp-model:2026-hw5 .
docker run --rm -p 9696:9696 zoomcamp-model:2026-hw5
python q6_test.py
# {'conversion_probability': 0.769799, 'conversion': True}
curl -s http://localhost:9696/health
# {"status":"ok","model_sha256":"1646bbdc...29f1", ...}
```

## Notes

- `pipeline.bin` was pickled with scikit-learn 1.7.2. Loading it with another version can give
  warnings or different results, so use the locked environment.

## What I learned

<!-- TODO: write a few lines in my own words -->
