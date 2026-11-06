# Homework 1

## Setup

Use Python 3.11 or 3.12. From this assignment directory:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Windows, activate with `.venv\Scripts\activate`. CPU execution is sufficient.

## Files and execution

- `HW1_4.ipynb`: regression residual histograms, Q–Q plots, and normality tests.
- `HW1_5.ipynb`: logistic/probit classification and linear regression with MSE and Student-t losses, using per-sample SGD.
- `mcs_ds_edited_iter_shuffled.csv`: ALE dataset; the first four columns predict `ale`; `sd_ale` is excluded.

Data source: [UCI Average Localization Error dataset](https://archive.ics.uci.edu/dataset/844/average+localization+error+(ale)+in+sensor+node+localization+process+in+wsns). Breast cancer data are bundled with scikit-learn and loaded with `load_breast_cancer()`.

### Interactive execution

From this assignment directory:

```bash
jupyter lab
```

Open either notebook and run all cells in order using the installed environment. Keep the notebook working directory set to this assignment directory.

### Noninteractive execution

From this assignment directory:

```bash
python -m jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=3600 HW1_4.ipynb
python -m jupyter nbconvert --to notebook --execute --inplace --ExecutePreprocessor.timeout=3600 HW1_5.ipynb
```

Per-sample SGD involves many small updates, so Homework 1 problem 5 may take several minutes or longer depending on hardware. Problem 4 saves PNG plots and a results CSV beside its data. Problem 5 displays its tables and training curves in the notebook. Random seeds are fixed at 42; small numerical differences across software versions are possible.
