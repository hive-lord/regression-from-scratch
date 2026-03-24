# Regression From Scratch

This project started as my attempt to implement linear regression manually on TSLA data and then compare it against sklearn.

## How I Started

- I began with a pure from-scratch version using NumPy + pandas only.
- I built the flow step by step: data loading, feature engineering, scaling, cost function, gradients, and gradient descent.
- After that, I built a sklearn version with the same feature pipeline to compare results fairly.

## Inspiration

The from-scratch implementation is inspired by Andrew Ng's supervised machine learning style:

- explicit parameters (`w`, `b`)
- explicit cost and gradient updates
- iterative gradient descent instead of a black-box fit

## AI Assistance Note

I used AI assistance to clean up and rename variables because I was getting confused with naming and consistency while switching between notebooks.

## Structure

- `TSLA.csv` - dataset
- `model-from-scratch.ipynb` - manual linear regression implementation
- `model-from-slklearn.ipynb` - sklearn linear regression implementation
- `compare.ipynb` - main output notebook with final side-by-side metric comparison

## Tech Stack

- Python
- NumPy
- pandas
- scikit-learn
- matplotlib

## Current Model Faults

- It is still a linear model, so non-linear market behavior is not captured well.
- The split is a simple holdout split; it does not test robustness across multiple time windows.
- Feature set is basic; important market/context signals may be missing.
- Hyperparameters in the from-scratch model are manually chosen and may not be optimal.
- Evaluation is focused on a few summary metrics and not full trading-oriented validation.

## How I Can Improve It

- Add stronger time-series features (lag windows, rolling volatility, momentum variations).
- Use proper walk-forward or rolling validation instead of a single split.
- Tune hyperparameters (`alpha`, `lambda`, iterations) systematically.
- Test regularized alternatives (Ridge/Lasso) and compare stability.
- Try non-linear models for benchmark comparison.
- Add residual/error plots and more diagnostics to understand failure cases better.

Main output: `compare.ipynb`
