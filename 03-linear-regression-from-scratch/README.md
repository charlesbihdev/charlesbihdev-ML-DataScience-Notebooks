# Linear Regression from Scratch

A `LinearRegression` class implemented from first principles in **NumPy** — no
scikit-learn estimator — trained with **batch gradient descent**.

## Files
- `linear_regression.py` — the model: `fit` (gradient descent over analytical
  gradients for the weights and bias) and `predict`.
- `train.py` — trains on a synthetic regression dataset, reports **mean squared
  error**, and plots the fitted regression line.

## Run
```bash
pip install numpy scikit-learn matplotlib
python train.py
```

## Why it matters
Implementing the cost minimization and gradient updates by hand demonstrates the
math underneath the library call, not just the API.
