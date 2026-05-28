# Analysis Guide

Complete guide to all analysis features in the Nexus Mods Rewards notebook.

## Data Loading and Cleaning

The notebook automatically:
- Reads the CSV file
- Parses dates from `Mon YYYY` format
- Drops the `Your Reward` column if identical to `Mod Rewards`
- Handles missing values in `Unique Downloads`

## Analysis Sections

### Rolling Statistics
- **3-month and 6-month moving averages**: Smooth out short-term variations
- **Rolling standard deviation**: Measure of volatility over time
- Helps identify whether trends are stable or changing

### Outlier Detection
- **IQR method**: Flags points outside 1.5x the interquartile range
- **Z-score method**: Flags points with Z-score > 2
- Outliers are marked on time series plots

### Trend Forecasting
- **Linear regression**: Fits a trend line to the data
- **95% confidence intervals**: Range where future values are likely to fall
- Extrapolates 6 months into the future

### Mann-Kendall Trend Test
- Tests for monotonic (consistent) upward or downward trend
- Reports: trend direction, p-value, and significance
- P-value < 0.05 = statistically significant trend

### Seasonal Decomposition
- Decomposes data into trend, seasonal, and residual components
- Helps understand cyclical patterns (e.g., higher downloads during game updates)

### Reward Efficiency
- Computes rewards per download over time
- Identifies periods of higher or lower efficiency

### Milestone Tracking
- Tracks cumulative downloads and rewards
- Shows when milestones were reached (e.g., 1000, 5000, 10000 downloads)

## Visualizations

| Chart | Purpose |
|-------|---------|
| Time series with outliers | Identify unusual months |
| Forecast | Future trend projection |
| Growth rates | Month-over-month changes |
| Correlation | Downloads vs rewards relationship |
| Seasonal patterns | Monthly patterns across years |
| Year-over-year | Compare same months across years |
| Heatmap | Monthly values as color grid |
| Distribution | Histogram of monthly values |
| Cumulative | Running totals over time |

## Output

All files are saved to `analysis_output/`:
- **CSV files**: Processed data, forecasts, monthly/quarterly/yearly aggregates
- **PNG files**: All chart visualizations

## Tips

- More data = more reliable analysis. At least 12 months recommended
- Seasonal patterns may not be visible with less than 2 years of data
- Outliers don't always mean errors — they could reflect genuine events (game update, mod feature)

---

[Back to Documentation](../README.md)
