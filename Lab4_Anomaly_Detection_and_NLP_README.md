# Lab 4 - Anomaly Detection & NLP (Oil & Gas Operations)

**Notebook:** [Lab4_Anomaly_Detection_and_NLP.ipynb](https://github.com/waqarahmed1/data-science-with-python/blob/main/Lab4_Anomaly_Detection_and_NLP.ipynb)

## Objective
- Part A: Detect anomalies in sensor time-series with Isolation Forest.
- Part B: Apply NLP to incident/maintenance reports (keywords, sentiment, optional classifier).

## Recommended datasets
- Time-series: NAB dataset (https://github.com/numenta/NAB) or a local CSV of sensor readings.
- Text: Kaggle incident/safety report datasets (download locally). The notebook includes synthetic fallbacks if offline.

## Prerequisites
- Python 3.10+ with `pandas`, `numpy`, `matplotlib`, and `scikit-learn` installed (`pip install pandas numpy matplotlib scikit-learn`).
- Jupyter Lab/Notebook.

## Run the lab
1) Provide time-series and text CSVs locally (or use the synthetic generators).
2) `jupyter lab` and open `Day 2/Labs/Lab4_Anomaly_Detection_and_NLP.ipynb`.
3) Execute cells in order; for Part B, ensure text columns are named clearly (e.g., `text` or `description`).

## Lab flow
- Load time-series data and visualize trends.
- Create rolling/statistical features to stabilize the Isolation Forest detector.
- Fit Isolation Forest, tune contamination, and plot detected anomalies.
- Load incident text data.
- Analyze keyword frequency with simple regex tokenization.
- Score sentiment using an offline baseline.
- Optional: build a TF-IDF + Logistic Regression classifier and inspect the classification report.

## Outputs
- Anomaly flags/plots for the provided time-series.
- Keyword/sentiment summaries; optional classification report for incident texts.

## Checkpoints
- Why add rolling features for anomaly detection?
- How would you tune contamination for a real operations environment?
- What are limitations of rule-based sentiment approaches?

## Tips
- Start with a conservative contamination setting; increase only after visual validation of anomaly plots.
- For text, clean noisy fields (HTML, repeated punctuation) before vectorization to improve signal.
