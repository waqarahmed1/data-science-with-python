# Lab 1 - Python & Pandas Foundations (Oil & Gas Context)

**Notebook:** [Lab1_Python_and_Pandas_Foundations.ipynb](https://github.com/waqarahmed1/data-science-with-python/blob/main/Lab1_Python_and_Pandas_Foundations.ipynb)

## Objective
- Practice the Python + Pandas workflow for loading, inspecting, cleaning, and transforming tabular oil & gas data.
- Produce a cleaned dataset that will feed Lab 2.

## Data options
- Kaggle CSV (search for "oil production" / "oil and gas production").
- Synthetic fallback generator included in the notebook for offline use.

## Prerequisites
- Python 3.10+ with `pandas` and `numpy` installed (`pip install pandas numpy`).
- Jupyter Lab/Notebook available (`pip install jupyterlab`).

## Run the lab
1) `git clone https://github.com/waqarahmed1/data-science-with-python.git` and `cd data-science-with-python`.
2) Optional: `python3 -m venv .venv && source .venv/bin/activate`.
3) `pip install pandas numpy jupyterlab` (add `matplotlib` if you want quick plots).
4) Launch Jupyter: `jupyter lab` and open `Day 1/Labs/Lab1_Python_and_Pandas_Foundations.ipynb`.
5) Choose a CSV (or rely on the synthetic fallback) when prompted and run cells top-to-bottom.

## Lab flow
- Setup imports and paths.
- Load a local CSV or generate synthetic production data.
- Quick inspection (`head`, `info`, `describe`) to understand columns and dtypes.
- Cleaning tasks: parse date columns, coerce numeric types, replace placeholder values (e.g., `-999`), and handle missing values.
- Feature engineering for operational insights (ratios, rates, or other derived columns).
- Filtering and sorting to focus on fields/wells of interest.
- Groupby and aggregation to summarize production by field or date.
- Export the cleaned dataset for later labs to `outputs/lab1_cleaned_oil_production.csv`.

## Outputs
- `outputs/lab1_cleaned_oil_production.csv` (input to Lab 2).

## Checkpoints
- What does `df.info()` tell you that `df.describe()` does not?
- Why can replacing placeholder codes with `NaN` be important before analysis?
- When would `groupby().transform()` be preferred over `groupby().agg()`?

## Tips
- If you use a Kaggle dataset, confirm date columns parse correctly and numeric fields do not stay as strings.
- Create the `outputs/` folder if it does not exist so the export cell can write the CSV.
