# Lab 2 - Exploratory Data Analysis (EDA) & Data Curation

**Notebook:** [Lab2_EDA_and_Data_Curation.ipynb](https://github.com/waqarahmed1/data-science-with-python/blob/main/Lab2_EDA_and_Data_Curation.ipynb)

## Objective
- Explore the cleaned dataset, quantify quality issues, and curate data for downstream ML.
- Deliver a curated CSV with gaps handled, outliers checked, and basic augmentation performed.

## Data options
- Preferred: `outputs/lab1_cleaned_oil_production.csv` produced in Lab 1.
- Alternate: any oil & gas CSV from Kaggle (download locally).

## Prerequisites
- Python 3.10+ with `pandas`, `numpy`, and `matplotlib` installed (`pip install pandas numpy matplotlib`).
- Jupyter Lab/Notebook.

## Run the lab
1) From the repo root: ensure `outputs/lab1_cleaned_oil_production.csv` exists or place a Kaggle CSV locally.
2) `jupyter lab` and open `Day 1/Labs/Lab2_EDA_and_Data_Curation.ipynb`.
3) Point the loader to your CSV and execute cells in order.

## Lab flow
- Load the Lab 1 output (or chosen dataset) into Pandas.
- Examine missingness and summary statistics.
- Plot distributions and time-series trends by field to spot shifts.
- Compute correlations between key variables.
- Detect outliers using IQR rules and review their operational plausibility.
- Handle missing data with median fill + interpolation where appropriate.
- Simple data synthesis/augmentation to bolster later model training.
- Save curated output for ML to `outputs/lab2_curated_for_ml.csv`.

## Outputs
- `outputs/lab2_curated_for_ml.csv` (input to Lab 3).

## Checkpoints
- Why might correlation be misleading for time-series data?
- When is interpolation acceptable and when is it risky?
- How would you decide whether to cap, remove, or keep outliers in Oil & Gas?

## Tips
- Keep track of units when comparing fields (bbl/day vs m3/day) to avoid false outliers.
- Regenerate figures after each cleaning step to verify the effect.
