# Frequently Asked Questions

## Data

### What CSV format is expected?
See the [Quick Start](QUICK_START.md) for the required column format. Export your data from the Nexus Mods rewards page.

### Can I analyze multiple mods?
The current notebook analyzes a single mod's data. You can extend it by adding more CSV files and processing them in sequence.

## Analysis

### What is Mann-Kendall trend testing?
A statistical test that determines if there's a monotonic trend in your data (consistently increasing or decreasing). P-value < 0.05 means the trend is statistically significant.

### What are rolling statistics?
Moving averages and standard deviations computed over a sliding window (3 or 6 months). They smooth out short-term fluctuations to reveal longer-term trends.

### What is reward efficiency?
Reward points per download. Higher values mean you're earning more per download.

## Troubleshooting

### CSV won't load
- Check column names match exactly
- Ensure the file encoding is UTF-8
- Remove any header rows above the column names

### Charts look empty
- Ensure your CSV has enough data (at least 6 months)
- Check for missing values in the Downloads or Rewards columns

---

**Last Updated**: 2026-05-25
