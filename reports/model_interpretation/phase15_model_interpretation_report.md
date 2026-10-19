# Phase 15 — Corrected Model Interpretation Report

## Experiment setup
- Target: 3-month forward return (`forward_return_3m`), reconstructed from Phase 8 prices using a 63-observation horizon.
- Candidate predictors: momentum_21d, momentum_63d, benchmark_return_1d, benchmark_volatility_21d, benchmark_volatility_63d.
- Selected model by validation MAE: Training mean baseline.
- Held-out test observations with valid predictions: 9,412.

## Held-out test metrics
- MAE: 0.143784
- RMSE: 0.184964
- R²: -0.044950
- Actual mean return: -0.009888
- Mean predicted return: 0.028474
- Mean prediction bias (predicted − actual): 0.038362

## Baseline comparison
{
  "status": "could not identify baseline and model rows"
}

## Interpretation and limitations
- Metrics describe this held-out historical period only.
- Return prediction errors can vary by month and ticker; inspect the saved breakdowns.
- Feature-name screening is not proof that every feature was available at prediction time.
- A regression score does not establish profitability after transaction costs, slippage, taxes, or portfolio constraints.
- This report is educational research, not investment advice.

## Outputs
- `recalculated_selected_model_metrics.csv`
- `baseline_assessment.json`
- `residual_summary.csv`
- `monthly_test_performance.csv`
- `ticker_test_performance.csv` (if enough observations)
- `residual_distribution.png`
- `actual_vs_predicted.png`