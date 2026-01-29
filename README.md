# energy-market-wind-solar-analysis
Data-driven analysis of global electricity generation mix with a focus on wind and solar adoption. Features PCA + KMeans clustering, trend analysis, and forecasting on UN-style panel data.

# Energy Market Wind & Solar Analysis (1990–2024)

# Overview
This repository provides a supporting analytical appendix for energy market briefings on wind and solar adoption trends.
The analysis uses synthetic data structured to mirror UN Energy Statistics, enabling reproducible workflows for trend analysis, clustering, and short-horizon forecasting.

# Objectives
> Analyze long-run wind and solar electricity adoption (1990–2024)
> Compare electricity mix evolution across countries and regions
> Identify electricity-mix archetypes using PCA + clustering
> Produce policy-neutral, short-horizon forecasts
> Demonstrate a UN-style, reproducible analytics workflow


# Key Assumptions & Hypotheses

1. Harmonized UN-style data is suitable for cross-country comparison (minor lags expected).
2. Distributed / off-grid solar PV may be under-reported; analysis focuses on utility-scale signals.
3. Wind and solar adoption follow logistic / trend growth patterns.
4. PCA + K-Means (k ≈ 4–6) is sufficient for first-pass electricity-mix clustering.
5. Forecasts shown are base-case (policy-neutral).
6. Short missing gaps are interpolated; long gaps are flagged and excluded from modeling.

# Data Description
1. energy_mix_wide_22k.csv (22,750 rows)
   Format: Country × Year (wide)
   Best for: Analysis, visualization, modeling
Includes:
> Total electricity generation (GWh)
> Generation by source (coal, gas, hydro, nuclear, wind, solar)
> Electricity mix shares
> Installed wind & solar capacity (MW)
> Electricity demand & price index

2. energy_panel_unstyle_22k.csv (204,750 rows)
   Format: Long UN-style panel
   Best for: Reproducibility, appendices, automated reporting

# Analytical Workflow
1. Data validation & missingness diagnostics
2. Trend analysis of wind and solar adoption
3. Regional & income-group comparisons
4. Electricity-mix clustering (PCA + K-Means)
5. Short-horizon forecasts (base case)
6. Limitations & caveats
7. Appendix tables (UN-style long format)

# Methods & Tools
> Python 3
> Pandas, NumPy
> Matplotlib / Seaborn
> Scikit-learn (PCA, K-Means)
> Statsmodels (trend forecasting)

# Outputs
> Time-series trend charts
> Electricity-mix cluster visualizations
> Country archetype summaries
> Forecast trajectories with uncertainty discussion
> UN-style appendix tables


# How to Run
git clone https://github.com/yourusername/energy-market-wind-solar-analysis.git
cd energy-market-wind-solar-analysis
pip install -r requirements.txt
jupyter notebook

# Limitations
Synthetic data is illustrative only
No explicit policy or price elasticity modeling
Forecasts are baseline, not scenario-based

# Future Extensions
Policy-driven scenarios (accelerated / delayed adoption)
Capacity-to-grid constraint modeling
Storage and curtailment integration
Regional power-market segmentation
