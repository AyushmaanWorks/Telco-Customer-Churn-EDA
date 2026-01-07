# Telco Customer Churn – Exploratory Data Analysis

This repository contains an exploratory data analysis (EDA) of the Telco Customer Churn dataset.  
The goal is to understand customer behavior patterns and identify factors associated with churn using clear visualizations and structured analysis.

## Dataset
- **Name:** Telco Customer Churn
- **Target variable:** `Churn` (Yes / No)
- **Features:** Customer demographics, services subscribed, tenure, and billing information
  
**Source:** Kaggle — Telco Customer Churn (BlastChar)  
Download: https://www.kaggle.com/datasets/blastchar/telco-customer-churn :contentReference[oaicite:6]{index=6}

### Download (recommended: Kaggle API)
1. Install Kaggle CLI: `pip install kaggle`
2. Create API token: Kaggle → Account → “Create New Token”
3. Place `kaggle.json` at `~/.kaggle/kaggle.json`
4. Run:
   ```bash
   kaggle datasets download -d blastchar/telco-customer-churn -p data --unzip

## Structure
- `tcc_eda_portfolio_completed.ipynb` – Main notebook containing:
  - Dataset loading and structural audit
  - Data cleaning and preprocessing
  - Univariate and bivariate analysis
  - Churn-based comparisons for numerical and categorical features
  - Correlation analysis (heatmap)
  - Segment-level churn analysis (risk groups)
  - High-risk / high-value churner identification
  - Key business insights and conclusions

## Analysis Approach
1. Structural audit (data types, missing values, cardinality)
2. Cleaning and standardization
3. Distribution analysis of numerical and categorical variables
4. Feature-wise comparison against churn
5. Correlation analysis to understand feature relationships
6. Segment analysis to identify high-risk customer groups
7. Insight extraction with business relevance

## Key Insights
- Customers with longer tenure are less likely to churn.
- Churned customers tend to have higher monthly charges.
- A small group of high-value, long-tenure customers still churn, representing high-risk, high-value users.
- Service type and contract duration strongly influence churn behavior.
- Certain feature combinations (example: contract type × internet service) reveal clear high-risk segments.

## Portfolio Enhancements
- Churn-rate tables (percentage-based comparisons, not only raw counts)
- Contract × InternetService churn-rate pivots to find “risk pockets”
- Add-on services analysis (filtered correctly to avoid “No internet service” distortion)
- Consolidated “highest-risk segments” table with minimum sample-size filtering
- Identification of “high-risk, high-value churners” for targeted investigation

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn

## Usage
Open the notebook and run cells sequentially:

```bash
jupyter notebook tcc_eda_portfolio_completed.ipynb
