# Phase 24 — Robustness Checks & Error Analysis

## Overall
- Test rows: 9412
- Tickers: 52
- MAE: 0.145430
- RMSE: 0.187049
- R²: -0.068638
- Mean prediction bias (predicted - actual): 0.042465

## Highest-error tickers
- ASG: MAE 0.352682
- STP: MAE 0.293016
- KMD: MAE 0.274676
- PWR: MAE 0.258991
- ANN: MAE 0.229782

## Interpretation
- These are descriptive diagnostics of the held-out test period, not a new tuning loop.
- Forward-return targets overlap over 63 observations, so errors are temporally dependent.
- The baseline outperformed Ridge on the Phase 23 test metrics; do not claim the current model adds predictive value.
- Ticker/month patterns may be unstable and should not be interpreted as future forecasts.