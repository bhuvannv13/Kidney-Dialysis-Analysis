# Kidney Dialysis Data Analysis

Coursework notebooks exploring healthcare data with Python: building and analysing patient treatment datasets, and comparing simple classifiers for dialysis-related outcomes.

> Learning project. Not intended for clinical use.

## Notebooks

| Notebook | What it does |
|---|---|
| `HCA_Project.ipynb` | Generates a synthetic dataset of 1,000 patient records, then trains a decision tree and a logistic regression model to predict `Need Dialysis`. |
| `Kidney Dialysis.ipynb` | Cleans a kidney dialysis dataset, one-hot encodes the categorical fields, and compares logistic regression, decision tree and gradient boosting for predicting `Symptom Relief`. |
| `HCA_CSV.ipynb` | Loads and inspects a hospital admissions table derived from MIMIC-III. |

## Results

Accuracy recorded in the notebooks is close to chance: about 0.25 for the symptom-relief models and about 0.53 for the decision tree on dialysis need. The dataset in `HCA_Project.ipynb` is randomly generated, so there is no real signal for a model to learn there. The value of this project is the end-to-end workflow (cleaning, encoding, training and evaluation) rather than the scores.

## Running the notebooks

```bash
pip install pandas numpy matplotlib seaborn scikit-learn notebook
jupyter notebook
```

The notebooks read CSV files from local paths and the data files are not included in this repository. Update the `pd.read_csv` paths to point at your own copies. `HCA_Project.ipynb` can regenerate its synthetic dataset from its first cell.

## Possible improvements

- Use a real, documented dialysis dataset
- Add cross-validation and metrics beyond accuracy
- Add a `requirements.txt` and relative data paths
