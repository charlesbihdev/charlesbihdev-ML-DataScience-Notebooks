# Retail Sales Analysis

Exploratory data analysis of a retail **Superstore** dataset (`train.csv`).

## What it does
- Cleans the data: fills missing postal codes, fixes dtypes, checks for duplicates.
- Profiles **customer segments** (Consumer / Corporate / Home Office) by count and sales.
- Finds **top spenders** and **repeat-order frequency** per customer.
- Breaks down sales by **shipping mode**, **state**, and **product category / sub-category**.
- Parses order dates to chart **year-over-year sales trends**.

## Tools
pandas · matplotlib · seaborn · plotly

## Run
Open `retail_sales_analysis.ipynb` in Jupyter or Colab. Update the `read_csv`
path to point at `train.csv` in this folder.
