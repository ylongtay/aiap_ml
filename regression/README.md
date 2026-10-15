# HDB Resale Transactions Analysis

This repository contains exploratory analysis of Singapore HDB resale
transactions. The dataset is a CSV of transaction records, and the Jupyter
notebooks explore its columns, clean selected fields, and visualize price
patterns and relationships.

## Repository contents

- `data/resale_transactions.csv` — transaction data. Columns include the
  transaction month, flat type, block, street, storey range, floor area,
  lease information, resale price, and town/flat-model identifiers and names.
- `jupyter/preliminary_data_exp.ipynb` — initial inspection and summary
  statistics.
- `jupyter/data_cleaning.ipynb` — cleaning and filling selected missing town
  and flat-model names.
- `jupyter/univariate_analysis.ipynb` — distributions and counts, including
  resale price and transaction month.
- `jupyter/bivariate_analysis.ipynb` — comparisons between resale price and
  other features, including flat type and floor area.
- `jupyter/correlation_analysis.ipynb` — Pearson and Spearman correlation
  analysis.
- `src/` — reserved Python modules and configuration; these files are
  currently empty, so there is not yet a command-line application or model
  training pipeline.

## Getting started

Use Python 3 with JupyterLab, pandas, matplotlib, and seaborn installed. For
example, create and activate a virtual environment, then install the notebook
dependencies:

```bash
python -m venv .venv
```

On Windows:

```powershell
.venv\Scripts\Activate.ps1
python -m pip install jupyterlab pandas matplotlib seaborn
```

On macOS or Linux:

```bash
source .venv/bin/activate
python -m pip install jupyterlab pandas matplotlib seaborn
```

Start Jupyter from the repository root:

```bash
jupyter lab jupyter/
```

Open a notebook and run its cells. The notebooks load the CSV using the
relative path `../data/resale_transactions.csv`, so keep the notebook in the
`jupyter/` directory.

## Current scope

The repository currently supports interactive data exploration through the
notebooks. The scripts in `src/` do not yet prepare data or train a regression
model; run the notebooks for the analyses that are implemented.