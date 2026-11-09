# Mutual Fund Analysis & Ranking

A data-analysis project that cleans a dataset of Indian mutual funds, explores it, and ranks every fund using a weighted **Composite Score** built from returns, cost, and risk-adjusted performance metrics.

## Overview

The notebook (`mutualfundsprojectsimrn.ipynb`) walks through a complete data-analysis workflow:

1. **Load** the dataset (`comprehensive_mutual_funds_data.csv`, 814 funds × 20 columns).
2. **Inspect** shape, columns, data types, unique values, missing values, and duplicates.
3. **Clean** the data (handle missing values, strip `%` and `,` characters, convert text to numbers).
4. **Explore** categories, AMCs (fund houses), min/max values, and feature correlations (heatmap).
5. **Engineer features**: normalise key metrics, compute a Composite Score, and rank funds.
6. **Export** the cleaned and ranked data to Excel.

## Dataset

File: `comprehensive_mutual_funds_data.csv` (not included in this repo; place it in the project root).

| Column | Description |
|---|---|
| `scheme_name` | Name of the mutual fund scheme |
| `min_sip` / `min_lumpsum` | Minimum SIP / lump-sum investment amount |
| `expense_ratio` | Annual fund management fee (%) |
| `fund_size_cr` | Fund size (₹ crore) |
| `fund_age_yr` | Age of the fund (years) |
| `fund_manager` | Fund manager name |
| `sortino`, `sharpe` | Risk-adjusted return ratios |
| `alpha`, `beta` | Performance vs. benchmark / market sensitivity |
| `sd` | Standard deviation (volatility) |
| `risk_level`, `rating` | Risk label and fund rating |
| `amc_name` | Asset management company |
| `category`, `sub_category` | Fund classification |
| `returns_1yr`, `returns_3yr`, `returns_5yr` | Annualised returns over 1, 3, and 5 years |

## Methodology

### Data cleaning
- `returns_3yr` (~2.6% missing) and `returns_5yr` (~20.5% missing) filled with the **mean**.
- All numeric columns: `%` and `,` removed, converted with `pd.to_numeric(errors="coerce")`, remaining gaps filled with the **median**.
- `-` placeholders replaced with `NaN`, then median-filled; remaining text gaps set to `"Unknown"`.

### Composite Score
Each of the 8 features is scaled to 0–1 with `MinMaxScaler`. Since lower is better for **expense ratio** and **beta**, those two are inverted (`1 - value`). The score is then a weighted sum:

| Feature | Weight |
|---|---|
| `returns_1yr` | 0.20 |
| `returns_3yr` | 0.20 |
| `returns_5yr` | 0.20 |
| `expense_ratio` (inverted) | 0.15 |
| `sharpe` | 0.10 |
| `sortino` | 0.05 |
| `alpha` | 0.05 |
| `beta` (inverted) | 0.05 |

Funds are then ranked (dense ranking, highest score first) and the top 10 / 20 / 30 funds are extracted.

## Output

- `MutualFund_Clean.xlsx`: cleaned dataset with `Composite Score` and `Rank` columns, sorted by score.

## Getting Started

### Prerequisites
- Python 3.10+
- Jupyter (JupyterLab or Notebook)

### Installation

```bash
# 1. (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 2. Install the pinned dependencies
pip install -r requirement.txt

# 3. Install packages the notebook uses that are not in requirement.txt
pip install scikit-learn seaborn matplotlib openpyxl
```

> **Note:** `requirement.txt` does not currently list `scikit-learn`, `seaborn`, `matplotlib`, or `openpyxl`, which the notebook needs (for `MinMaxScaler`, plotting, and `to_excel`). Adding them to the file is recommended.

### Run

```bash
jupyter lab
```

Open `mutualfundsprojectsimrn.ipynb`, make sure the CSV is in the same folder, and run all cells.

## Project Structure

```
.
├── mutualfundsprojectsimrn.ipynb        # Analysis notebook
├── requirement.txt                      # Python dependencies
├── comprehensive_mutual_funds_data.csv  # Input data (add this yourself)
└── MutualFund_Clean.xlsx                # Generated output
```

## Tech Stack

Python · pandas · NumPy · scikit-learn · seaborn · Matplotlib · Jupyter

## Disclaimer

This project is for educational and analytical purposes only and is not financial advice. Past returns do not guarantee future performance.