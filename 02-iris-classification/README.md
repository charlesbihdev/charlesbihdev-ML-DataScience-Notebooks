# Iris Classification

The classic **Iris** dataset (`iris.csv`) worked end to end.

## What it does
- **EDA:** summary statistics, per-feature histograms, class-wise scatter plots,
  and a correlation heatmap.
- **Preprocessing:** drops the ID column, label-encodes the species target.
- **Modeling:** an 80/20 train/test split with two classifiers —
  **Logistic Regression** and **K-Nearest Neighbors** — scored on test accuracy.

## Tools
pandas · numpy · matplotlib · seaborn · scikit-learn

## Run
Open `iris_classification.ipynb` in Jupyter or Colab and point the `read_csv`
path at `iris.csv` in this folder.
