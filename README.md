# DATA37711 — Machine Learning 1

Course homework code. Each assignment is stored under `homework_N/`.

## Setup

Use Python 3.11 or 3.12. CPU execution is sufficient.

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Windows, activate with `.venv\Scripts\activate`.

## Homework 1

- `homework_1/HW1_4.ipynb`: regression residual histograms, Q–Q plots, and normality tests.
- `homework_1/HW1_5.ipynb`: logistic/probit classification and linear regression with MSE and Student-t losses, using per-sample SGD.
- `homework_1/mcs_ds_edited_iter_shuffled.csv`: ALE dataset; the first four columns predict `ale`; `sd_ale` is excluded.

Data source: [UCI Average Localization Error dataset](https://archive.ics.uci.edu/dataset/844/average+localization+error+(ale)+in+sensor+node+localization+process+in+wsns). Breast cancer data are bundled with scikit-learn and loaded with `load_breast_cancer()`.

### Interactive execution

From the repository root:

```bash
jupyter lab
```

Open either notebook and run all cells in order using the installed environment. Paths work from either the repository root or `homework_1/`.

### Noninteractive execution

From the repository root:

```bash
python -m jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=3600 homework_1/HW1_4.ipynb
python -m jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=3600 homework_1/HW1_5.ipynb
```

Per-sample SGD involves many small updates, so Homework 1 problem 5 may take several minutes or longer depending on hardware. Problem 4 saves PNG plots and a results CSV beside its data. Problem 5 displays its tables and training curves in the notebook. Random seeds are fixed at 42; small numerical differences across software versions are possible.

Lecture PDFs, assignment PDFs, and the original `HW1/` working directory are excluded from version control.
