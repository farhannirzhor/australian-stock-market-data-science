# Australian Stock Market Analytics & Return Modeling

## Executive summary

This project builds an end-to-end workflow for analyzing Australian stock data, engineering historical price features, studying company groups, and evaluating a three-month forward-return regression experiment.

The final predictive target is `forward_return_3m`, defined over 63 future observations per ticker. The Phase 23 model was selected using validation MAE and evaluated on a held-out chronological test period.

## Final model evaluation

- Model selected on validation MAE: **Ridge Regression**
- Test observations: **9412**
- Number of predictors: **18**
- Test MAE: **0.145430**
- Baseline test MAE: **0.143784**
- Test RMSE: **0.187049**
- Test R-squared: **-0.068638**
- Actual mean test return: **-0.009888**
- Mean predicted test return: **0.032577**
- Did the model beat the baseline on MAE? **False**

### Interpretation

The selected model did **not** beat the mean baseline on held-out test MAE. The test R-squared is negative, and the mean prediction is higher than the realized mean return in the test period. Therefore, the current experiment does not establish useful incremental predictive performance over the baseline.

## Workflow

The project phases cover:
1. Data understanding and workbook inspection.
2. Data cleaning and quality audits.
3. Financial feature engineering.
4. Exploratory data analysis.
5. Statistical analysis.
6. Exploratory company segmentation.
7. Predictive-task feasibility review.
8. Historical market-data acquisition.
9. Forward-return target engineering.
10. Predictive feature preparation.
11–23. Model development, validation, feature audits, and final held-out evaluation.
24. Robustness checks and error analysis.
25. Final documentation and portfolio packaging.

## Methodology overview

The main modeling target is a three-month forward return based on 63 future price observations per ticker. The workflow uses chronological train, validation, and test periods. Model selection is based on validation MAE; the final selected model is refitted on train plus validation before test evaluation.

The selected feature list contains 18 predictors, primarily momentum, volatility, price-to-moving-average ratios, benchmark returns, and relative momentum.

## Limitations

- The current model does not outperform the mean baseline on the held-out test MAE.
- Negative test R-squared indicates weak out-of-sample explanatory performance.
- Forward-return windows overlap, so observations are not independent.
- Feature-name screening alone cannot prove that all features were available at prediction time; source formulas and benchmark alignment require review.
- Performance on one historical period is not evidence of future profitability.
- This project is for educational and research purposes, not investment advice.

## Recommended future work

- Verify point-in-time feature provenance and benchmark date alignment.
- Use walk-forward validation with purging/embargo for overlapping labels.
- Establish a documented baseline protocol before testing new features.
- If further modeling is attempted, reserve a new untouched future period for final evaluation.
- Explore ranking or classification targets only if they are defined in advance and validated without leakage.

## Reproducibility

See `artifact_inventory.csv`, `limitations_register.csv`, and `reproducibility_checklist.md` in the `reports/final_documentation/` directory. Preserve the phase outputs and record package versions and data retrieval dates before publishing.

---
**Disclaimer:** Historical research only. This report is not financial or investment advice.
