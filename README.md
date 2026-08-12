# Customer Churn Analysis
A Python data analysis project exploring customer churn using Pandas, SQLite, and Matplotlib/Seaborn, covering data cleaning, feature engineering, churn metrics, and visualizations.
## Features
- Data import from a SQLite database, with fallback to rebuild it from a raw Excel file
- Data cleaning: renaming columns, dropping unused fields, fixing data types, standardizing categories, filling missing values
- Feature engineering: churn flag, churn risk tiers, merged customer/subscription/support dataset
- Key churn metrics: churn rate, retention rate, ARPU, average tenure, revenue at risk, escalation rate
- Correlation analysis between support escalations and churn
- Visualizations: churn trend over time, churn by plan type and state, correlation heatmaps, pairplots, category plots
- Pivot tables summarizing churn and revenue by plan type
## Tech Stack
- Python 3
- Pandas / NumPy
- Matplotlib / Seaborn
- SQLite3
- Jupyter Notebook
## Project Structure
- `churn_analysis.ipynb` — main analysis notebook
- `customer_churn.db` — SQLite database with customer, subscription, and support tables
- `customer_churn_data_raw.xlsx` — raw source data used to build the database
## Setup
1. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```
2. Make sure `customer_churn.db` and `customer_churn_data_raw.xlsx` are in the project root.
3. Start Jupyter:
```bash
jupyter notebook
```
4. Open `churn_analysis.ipynb` and run all cells.
## Development
- `jupyter notebook` — launch the notebook environment
- `jupyter nbconvert --to script churn_analysis.ipynb` — export the notebook to a standalone Python script
## Notes
- The notebook reads directly from `customer_churn.db`. If the database is missing, it can be rebuilt from `customer_churn_data_raw.xlsx`.
- Churn risk tiers (`low` / `med` / `high`) are derived from a `churn_score` column using fixed thresholds.
- If the dataset contains real customer data, consider excluding `customer_churn.db` from version control or keeping the repository private.
## License
This repository is private by default. Update the license section if you open-source it.
