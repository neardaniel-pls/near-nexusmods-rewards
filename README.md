# Nexus Mods Rewards Analysis

Personal analysis tool for Nexus Mods download and rewards data. Parses CSV data, performs statistical analysis, trend forecasting, and generates visualizations.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11+](https://img.shields.io/badge/Python-3.11%2B-blue.svg)](https://www.python.org/)

## Overview

A Jupyter Notebook that analyzes your Nexus Mods download and rewards data over time. Includes rolling statistics, outlier detection, linear trend forecasting, Mann-Kendall trend testing, seasonal decomposition, and milestone tracking.

## Features

### Statistical Analysis
- **Rolling Statistics**: 3/6-month moving averages and standard deviation
- **Outlier Detection**: IQR + Z-score methods
- **Trend Testing**: Mann-Kendall test for monotonic trends
- **Seasonal Decomposition**: Trend, seasonal, and residual components

### Forecasting
- Linear trend forecasting with 95% confidence intervals
- 6-month forward projection

### Tracking
- Reward efficiency (rewards per download)
- Cumulative milestone tracking
- Growth rate analysis

### Visualizations
7 chart types: time series with outliers, forecasts, growth rates, correlation analysis, seasonal patterns, year-over-year comparison, and distribution analysis.

## Documentation

### [Documentation Hub](docs/README.md)
Guides and references

### [Quick Start Guide](docs/QUICK_START.md)
Get started in 2 minutes

### [Guides](docs/guides/)
- [Analysis Guide](docs/guides/analysis-guide.md)

### [FAQ](docs/FAQ.md)
Common questions

### [Contributing Guide](CONTRIBUTING.md)
How to contribute

## Installation

```bash
git clone https://github.com/neardaniel-pls/near-nexusmods-rewards.git
cd nexusmods-rewards

python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Usage

1. Place your `nexusmods_rewards.csv` in the project root
2. Run: `jupyter notebook nexusmods_rewards_analysis.ipynb`
3. All output goes to `analysis_output/`

### CSV Format

| Column | Description |
|--------|-------------|
| Month | Date in `Mon YYYY` format |
| Unique Downloads | Unique download count |
| Downloads | Total download count |
| Mod Rewards | Total reward points |
| Your Reward | Your reward share (optional) |

## Project Structure

```
nexusmods-rewards/
├── nexusmods_rewards_analysis.ipynb  # Main analysis notebook
├── nexusmods_rewards.csv             # Input data
├── requirements.txt                  # Python dependencies
├── analysis_output/                  # Generated outputs (gitignored)
└── docs/                             # Documentation
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

- [Report Bugs](https://github.com/neardaniel-pls/near-nexusmods-rewards/issues/new?template=bug_report.md)
- [Request Features](https://github.com/neardaniel-pls/near-nexusmods-rewards/issues/new?template=feature_request.md)

## Related Projects

- **[near-investing](https://github.com/neardaniel-pls/near-investing)**: Portfolio analysis and optimization tool
- **[near-fire-calculator](https://github.com/neardaniel-pls/calculadora-fire)**: FIRE calculator for the Portuguese market
- **[near-work-analysis](https://github.com/neardaniel-pls/near-work-analysis)**: Career path analysis tool
