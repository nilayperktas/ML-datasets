# Machine Learning Midterm Project

## Project Overview

This project compares classification and clustering algorithms using two datasets from scikit-learn:

- Breast Cancer Wisconsin (569 samples, 30 features, 2 classes)
- Wine (178 samples, 13 features, 3 classes)

## Classification Algorithms

- Decision Tree (max_depth: 2, 3, 5, 10, None)
- K-Nearest Neighbors (k: 1, 3, 5, 7, 11)
- Gaussian Naive Bayes (default parameters)

Each configuration is evaluated using three random seeds (42, 52, 62) and two feature representations (Scaled and Unscaled).

Model selection is based on mean validation Macro-F1, without using test results.

## Clustering

K-Means clustering is performed using 2 clusters for Breast Cancer and 3 clusters for Wine.

Clustering performance is evaluated using Adjusted Rand Index (ARI) and Silhouette Score.

## Data Preprocessing

- Stratified Train/Validation/Test splitting (approximately 70% / 10% / 20%)
- Fixed Test Set with random_state=42
- StandardScaler fitted only on Training data
- No feature selection or dimensionality reduction

## Project Files

- `breast_cancer.ipynb` — Breast Cancer analysis and experiments
- `wine.ipynb` — Wine analysis and experiments
- `figures/` — Visualizations and evaluation plots
- `results/` — Classification and K-Means CSV results
- `requirements.txt` — Python dependencies

## Installation

Install dependencies:

```bash
pip install -r requirements.txt
```

Open and run the notebooks in this order:

1. `breast_cancer.ipynb`
2. `wine.ipynb`

Run each notebook from top to bottom.

## Results

The project includes:

- 132 classification model fits
- 12 K-Means model fits
- 6 combined result CSV files
- Classification and clustering visualizations

## Reproducibility

Random seeds 42, 52 and 62 are used for the experiments. The same fixed Test Set is preserved across seeds for each dataset.