# Quick Start Guide

Get started with Nexus Mods Rewards Analysis in 2 minutes.

## Setup

```bash
git clone https://github.com/neardaniel-pls/near-nexusmods-rewards.git
cd nexusmods-rewards

python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Add Your Data

Place your `nexusmods_rewards.csv` in the project root with these columns:

| Column | Description |
|--------|-------------|
| Month | Date in `Mon YYYY` format (e.g., `Nov 2025`) |
| Unique Downloads | Unique download count |
| Downloads | Total download count |
| Mod Rewards | Total reward points |
| Your Reward | Your personal reward share |

## Run the Analysis

```bash
jupyter notebook nexusmods_rewards_analysis.ipynb
```

Run all cells. Output files are saved to `analysis_output/`.

## Next Steps

- [Analysis Guide](guides/analysis-guide.md) — All features explained
- [FAQ](FAQ.md) — Common questions

---

**Last Updated**: 2026-05-25
