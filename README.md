# Nexus Mods Rewards Analysis

Personal analysis of Nexus Mods download and rewards data over time. Parses, cleans, and visualizes monthly rewards trends with statistical analysis, forecasting, and outlier detection.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

Place your `nexusmods_rewards.csv` in the project root with the following columns:

| Column | Description |
|---|---|
| Month | Date in `Mon YYYY` format (e.g. `Nov 2025`) |
| Unique Downloads | Unique download count (ignored if empty) |
| Downloads | Total download count |
| Mod Rewards | Total reward points |
| Your Reward | Your personal reward share (dropped if identical to Mod Rewards) |

Open and run the notebook:

```bash
jupyter notebook nexusmods_rewards_analysis.ipynb
```

## Output

All generated files go to `analysis_output/`:

**CSVs** — cleaned data, forecast values, monthly/quarterly/yearly aggregates

**Visualizations** — time series with outliers, forecasts, growth rates, correlation, seasonal patterns, year-over-year, heatmaps, distribution, cumulative totals

## Analysis Features

- Rolling statistics (3/6-month moving averages, standard deviation)
- Outlier detection (IQR + Z-score)
- Linear trend forecasting with 95% confidence intervals
- Mann-Kendall trend testing
- Seasonal pattern decomposition
- Reward efficiency tracking (rewards per download)
- Milestone tracking (cumulative thresholds)
