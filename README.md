# Australian Stock Market Analytics & Return Modeling

An end-to-end Data Science project exploring Australian stock market data through financial data cleaning, exploratory data analysis, statistical testing, company segmentation, historical price analysis, feature engineering, and predictive modeling.

## Project Overview

This project investigates the structure and behavior of Australian listed companies and evaluates whether historical price-based features can help predict three-month forward returns.

The workflow covers the full Data Science process, from understanding and cleaning an original Excel dataset to evaluating predictive models on a chronological holdout period.

## Objectives

- Clean and validate company financial data.
- Engineer financial ratios and historical market features.
- Explore stock characteristics and relationships through EDA.
- Conduct statistical tests and correlation analysis.
- Explore company segmentation using clustering.
- Acquire historical market prices and construct forward-return targets.
- Compare regression models using chronological validation.
- Evaluate the selected model against a simple baseline.
- Document limitations and reproducibility requirements.

## Methodology

1. Data understanding and quality assessment
2. Data cleaning and validation
3. Financial feature engineering
4. Exploratory data analysis
5. Statistical analysis
6. Company segmentation
7. Predictive-task feasibility assessment
8. Historical market-data acquisition
9. Forward-return target engineering
10. Predictive feature preparation
11. Model development and evaluation
12. Leakage and feature-timing audits
13. Error analysis and robustness checks
14. Final research documentation

The project was implemented through a 25-phase notebook workflow.

## Technology Stack

- **Language:** Python
- **Data processing:** pandas, NumPy
- **Visualization:** Matplotlib
- **Machine learning:** scikit-learn
- **Statistical analysis:** SciPy, statsmodels
- **Historical market data:** yfinance
- **Development environment:** Jupyter Notebook, VS Code

## Predictive Modeling Results

The final experiment used `forward_return_3m`, a three-month forward-return target based on 63 future observations per ticker.

| Metric | Ridge Regression | Mean Baseline |
|---|---:|---:|
| Test MAE | 0.14543 | 0.14378 |
| Test RMSE | 0.18705 | 0.18496 |
| Test R² | -0.06864 | -0.04495 |

Ridge Regression was selected using validation MAE. However, it did not outperform the mean baseline on the held-out test set.

This is an important finding: the current experiment does not demonstrate reliable incremental predictive value over the baseline. The project reports this outcome transparently rather than presenting unsuccessful predictive performance as a successful forecasting system.

## Key Outputs

The repository includes notebooks and generated artifacts for:

- Data cleaning and validation
- Exploratory and statistical analysis
- Company segmentation
- Historical market data and engineered features
- Model evaluation and predictions
- Feature and leakage audits
- Error analysis and diagnostic visualizations
- Final research report and reproducibility checklist

## Limitations

- Results represent one historical evaluation period.
- Three-month forward-return targets overlap, so observations are not independent.
- Feature provenance and benchmark timing require careful verification.
- Negative test R² indicates weak out-of-sample explanatory performance.
- Historical results do not guarantee future performance.

## Reproducibility

1. Set up the Python environment and install the required dependencies.
2. Place the original dataset in the expected project location.
3. Run the notebooks in the appropriate phase order.
4. Verify intermediate datasets and audit reports.
5. Review the final model comparison and documented limitations.

Exact package versions and data-retrieval details should be recorded in the final environment documentation.

## Disclaimer

This project is for educational and research purposes only. It is not financial advice, an investment recommendation, or evidence of a profitable trading strategy.
