# Lab 3 - Pipeline Flow Prediction (Machine Learning)

**Notebook:** [Lab3_Pipeline_Flow_Prediction_ML.ipynb](https://github.com/waqarahmed1/data-science-with-python/blob/main/Lab3_Pipeline_Flow_Prediction_ML.ipynb)

## Objective
- Train and compare models that predict pipeline flow rate from sensor readings.
- Build an evaluation-ready dataset and capture baseline vs. ensemble performance.

## Recommended dataset
- Gas Pipeline Dataset from Kaggle: https://www.kaggle.com/datasets/garystafford/gas-pipeline-dataset (or use the synthetic fallback in the notebook).

## Prerequisites
- Python 3.10+ with `pandas`, `numpy`, `matplotlib`, and `scikit-learn` installed (`pip install pandas numpy matplotlib scikit-learn`).
- Jupyter Lab/Notebook.

## Run the lab
1) Place the pipeline CSV locally (or rely on the notebook's synthetic generator).
2) `jupyter lab` and open `Day 2/Labs/Lab3_Pipeline_Flow_Prediction_ML.ipynb`.
3) Execute cells sequentially; confirm the train/test split and target column before training.

## Lab flow
- Load sensor data and define feature columns vs. target (flow rate).
- Prepare data for ML: cleanup, encoding (if needed), and train/test split.
- Baseline model: Linear Regression.
- Tree-based model: Random Forest regressor.
- Compare models using RMSE and R².
- Plot predicted vs. actual to spot bias or heteroscedasticity.
- Review feature importance to understand drivers of flow.
- Save processed dataset or predictions to `outputs/lab3_pipeline_ml_dataset.csv` for reuse.

## Outputs
- `outputs/lab3_pipeline_ml_dataset.csv` (processed dataset and/or predictions for later experiments).

## Checkpoints
- Why is RMSE useful for operational forecasting?
- When might a linear model be preferred over Random Forest?
- What happens if the model is trained on a narrow operating range?

## Tips
- Keep the same preprocessing steps between baseline and Random Forest to ensure a fair comparison.
- If features have very different scales, consider standardization for the linear model.
