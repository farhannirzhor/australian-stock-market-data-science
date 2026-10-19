# Australian Stock Market Analytics & Return Modeling

An end-to-end Data Science project analyzing Australian listed companies, engineering market features, exploring company groups, and evaluating a three-month forward-return regression task.

## Project goals

- Inspect and clean company fundamentals from the original workbook.
- Engineer financial ratios and historical price-based features.
- Perform exploratory and statistical analysis.
- Explore company segmentation.
- Acquire historical market data and construct forward-return targets.
- Compare regression models using chronological validation.
- Evaluate the final selected model against a simple baseline.
- Document limitations and reproducibility.

## Final result

- **Target:** `forward_return_3m`
- **Selected model by validation MAE:** Ridge Regression
- **Predictors:** 18
- **Test observations:** 9412
- **Selected model test MAE:** 0.145430
- **Baseline test MAE:** 0.143784
- **Test R-squared:** -0.068638
- **Beat baseline on test MAE:** False

**Interpretation:** The selected model did not beat the mean baseline on test MAE. This project reports that outcome transparently and does not claim reliable return-prediction ability.

## Main tools

- Python
- pandas and NumPy
- Matplotlib
- scikit-learn
- SciPy and statsmodels (statistical analysis)
- yfinance (historical market data)
- Jupyter Notebook

## Suggested project structure

```text
.
├── data/
│   ├── raw/
│   ├── metadata/
│   └── processed/
├── notebooks/
├── reports/
│   ├── eda/
│   ├── statistical_analysis/
│   ├── company_segmentation/
│   ├── final_model_evaluation/
│   ├── robustness_error_analysis/
│   └── final_documentation/
└── README.md
```

## How to reproduce

1. Create/activate the Python environment used for the project.
2. Install required packages based on the notebook imports.
3. Place the original workbook in the expected project location.
4. Run notebooks in phase order and inspect each phase's output and warnings.
5. Confirm historical market-data retrieval and output files are present.
6. Review the final report and audit registers.

## Important limitations

- Historical evaluation only; not investment advice.
- The selected model did not beat the baseline on held-out test MAE.
- Forward-return labels overlap over 63 observations.
- Feature provenance and benchmark alignment require manual verification.
- One held-out period cannot establish future performance.

## Reports

See `reports/final_documentation/final_research_report.md` for the final research report and `artifact_inventory.csv` for an inventory of available outputs.
