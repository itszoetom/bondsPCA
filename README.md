# bondsPCA

# PCA Analysis of US Treasury Yield Curve

This notebook performs **Principal Component Analysis (PCA)** on historical US Treasury yields to identify the main patterns of movement in the yield curve. It decomposes the yield curve into interpretable components such as **level**, **slope**, and **curvature**.

## Overview

The US Treasury yield curve shows strong correlations between maturities, making it well-suited for PCA. This analysis extracts the first three principal components and interprets their economic meaning.

## Analysis Steps

1. **Data Preparation**
   - Load historical US Treasury yields for multiple maturities.
   - Align and clean data for PCA input.

2. **Principal Component Analysis**
   - Apply PCA to the time series of yields.
   - Calculate explained variance for each component.

3. **Visualization**
   - **Explained Variance Plot**: Shows how much variance each component explains.
   - **Loadings Plot**: Interprets each component in terms of yield curve shape.
     - **PC1 – Level**: Overall shift in interest rates.
     - **PC2 – Slope**: Steepening or flattening of the curve.
     - **PC3 – Curvature**: Mid-maturity hump or dip.
   - **PC Scores Over Time**: Tracks how each component's influence changes over time.

## Key Insights

- **PC1** generally accounts for the majority of variance and represents parallel shifts in the yield curve.
- **PC2** captures short- vs. long-term rate differences (slope).
- **PC3** highlights curvature changes, important in monetary policy analysis.

## Requirements

- Python 3.x
- pandas, numpy, matplotlib, seaborn, scikit-learn

## Usage

Open the notebook:

```bash
jupyter notebook pca_exp.ipynb
