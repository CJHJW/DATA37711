# Homework 2

## Setup

Use Python 3.11 or 3.12. From this assignment directory:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Windows, activate with `.venv\Scripts\activate`. CPU execution is sufficient.

## Files and execution

- [Written report](HW2.pdf): answers and experiment results for Homework 2.

- `problem1.ipynb`: conditional Gaussian MLP for taxi trip duration, with baseline comparisons and probability evaluation for trips under 45 minutes.
- `problem2.ipynb`: target encoding with linear regression, categorical embeddings, and their combination for retail quantities.
- `problem3.ipynb`: Random Kitchen Sinks with ridge regression and a one-hidden-layer MLP, including hyperparameter sweeps and fitted 3D surfaces.
- `rks_test_predictions.csv` and `mlp_test_predictions.csv`: 200 predictions each, one per row without a header, in the original `test.csv` order.

The required datasets are included: `taxi_trips.parquet`, `retail.csv`, and `train.csv` / `val.csv` / `test.csv`.

After installing this assignment's requirements, start Jupyter:

```bash
jupyter lab
```

Run each notebook from top to bottom with its working directory set to this assignment directory. Problem 3 regenerates the prediction CSVs and saves its plots there. Notebook outputs contain the experiment results; the written report is included as `HW2.pdf`.
