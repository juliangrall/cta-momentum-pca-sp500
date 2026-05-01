# CTA Strategy — Momentum & PCA on S&P 500

Construction and analysis of a quantitative trend-following (CTA) strategy on a 25-stock S&P 500 portfolio, combining moving-average momentum signals and principal component decomposition.

## Context
Project for the Asset Management & Data Mining course — M2 ISIFAR (Applied Mathematics for Finance), Université Paris-Cité, 2026.

## Data
Daily prices of 25 S&P 500 stocks from 2022-08-01 to 2025-08-01.

## Methods

### Part 1 — Momentum strategy
- Buy/sell signals from moving-average crossovers
- Position sizing with equal capital allocation per asset
- PnL calculation and portfolio value tracking
- Window optimization over m ∈ [5, 20] days using annualized return

### Part 2 — PCA-based CTA
- Log-returns standardization and PCA decomposition
- Scree plot for selecting principal components (k = 3)
- Eigenvector simplification via thresholding and sign extraction
- CTA strategy on simplified factor signals (sign of factor return)

### Part 3 — Correlation network analysis
- Correlation graph with threshold (ρ > 0.6)
- Minimum Spanning Tree based on metric distance d_ij = √(2(1 - ρ_ij))
- Visualization of cluster structure within the portfolio

## Key findings
- Optimal moving-average window depends heavily on stock-specific volatility
- Top 3 principal components explain a large share of return variance, suggesting common market factors
- MST reveals natural sector clustering of S&P 500 stocks

## Stack
Python, pandas, NumPy, scikit-learn, NetworkX, Matplotlib

## Files
- `Code.ipynb` — full implementation with plots
- `exercice-data-cta.pdf` — instructions

## How to run
```python
pip install pandas numpy scikit-learn networkx matplotlib
jupyter notebook
```
