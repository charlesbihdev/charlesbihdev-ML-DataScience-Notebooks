# Machine Learning & Data Science Notebooks

A portfolio of hands-on machine learning and data science projects, spanning
exploratory data analysis, classification, algorithms implemented from scratch,
and an end-to-end deep-learning face-recognition system with a serving API.

Each project is self-contained in its own folder with code, data (where small
enough to include), and a short write-up. Every notebook also opens directly in
Google Colab via the badge at the top of the notebook.

> **Author:** Charles Owusu Bih · [GitHub](https://github.com/charlesbihdev)

---

## Projects

| # | Project | Focus | Key tools |
|---|---------|-------|-----------|
| 01 | [Retail Sales Analysis](./01-retail-sales-analysis) | Exploratory data analysis & business insight | pandas, matplotlib, seaborn, plotly |
| 02 | [Iris Classification](./02-iris-classification) | Supervised classification & EDA | scikit-learn (Logistic Regression, KNN) |
| 03 | [Linear Regression from Scratch](./03-linear-regression-from-scratch) | Core ML algorithm implemented in NumPy | NumPy, gradient descent |
| 04 | [Face Recognition System](./04-face-recognition-system) | Deep learning pipeline: train → test → serve | PyTorch, FaceNet (MTCNN + InceptionResnetV1), SQLite, FastAPI |

---

### 01 · Retail Sales Analysis
Exploratory analysis of a retail "Superstore" dataset. Cleans and type-corrects
the raw data, then answers business questions through aggregation and
visualization: customer segments, top spenders, repeat-order frequency, shipping
mode usage, sales by category / sub-category / state, and year-over-year sales
trends.

**Skills shown:** data cleaning, `groupby` aggregation, feature engineering from
dates, and communicating findings with charts.

### 02 · Iris Classification
The classic Iris flower dataset worked end to end: EDA (histograms, class-wise
scatter plots, correlation heatmap), label encoding, a train/test split, and two
classifiers (Logistic Regression and K-Nearest Neighbors) with accuracy scoring.

**Skills shown:** the full supervised-learning workflow, from data understanding
to model evaluation.

### 03 · Linear Regression from Scratch
A `LinearRegression` class implemented from first principles in NumPy — no
scikit-learn estimator. Trains via batch gradient descent (analytical gradients
for weights and bias) and is validated against a synthetic regression dataset,
reporting mean squared error and plotting the fitted line.

**Skills shown:** the math behind ML — cost minimization, gradient descent, and
vectorized NumPy — not just calling a library.

### 04 · Face Recognition System
An end-to-end face-recognition pipeline built on **FaceNet** (MTCNN for face
detection + InceptionResnetV1 pretrained on VGGFace2 for embeddings):

1. **`1_train_embeddings.ipynb`** — detects faces in a person's images,
   generates 512-d embeddings, averages them into a single reference embedding,
   and stores it in a SQLite database.
2. **`2_test_recognition.ipynb`** — embeds unseen test images and matches them
   against the stored reference using cosine similarity, reporting a match
   percentage.
3. **`3_fastapi_service.ipynb`** — wraps the recognition logic in a FastAPI
   service (exposed publicly from Colab via ngrok).

**Skills shown:** applied deep learning, transfer learning with pretrained
models, embedding-based similarity, persistence, and model serving.

---

## Getting started

```bash
git clone https://github.com/charlesbihdev/charlesbihdev-ML-DataScience-Notebooks.git
cd charlesbihdev-ML-DataScience-Notebooks
pip install -r requirements.txt
```

Then open any notebook locally (`jupyter lab`) or click its **Open in Colab**
badge. For the pure-Python project (03), run:

```bash
cd 03-linear-regression-from-scratch
python train.py
```

## Tech stack
Python · NumPy · pandas · scikit-learn · matplotlib · seaborn · plotly ·
PyTorch · facenet-pytorch · FastAPI · SQLite

## Notes
- The face-recognition notebooks were built to run in Google Colab and read
  images from Google Drive; paths are set accordingly and can be adjusted for a
  local run.
- No secrets or credentials are committed — set your own ngrok token where noted.
