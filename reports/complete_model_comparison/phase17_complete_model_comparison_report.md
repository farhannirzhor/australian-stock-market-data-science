# Phase 17 — Complete Model Comparison

- Final selection based on validation: **Training mean baseline**
- Reason: No non-baseline model beat the baseline on validation MAE.
- Test observations: 9,412
- Test MAE: 0.142559
- Test RMSE: 0.183638
- Test R²: -0.030017
- Baseline test MAE: 0.142559
- Beats baseline test MAE: False

## Test comparison
                 model    n      MAE     RMSE        R2  actual_mean  predicted_mean  mean_prediction_bias
Training mean baseline 9412 0.142559 0.183638 -0.030017    -0.009888        0.021461              0.031349
      Ridge Regression 9412 0.144929 0.185742 -0.053759    -0.009888        0.021019              0.030907
     Linear Regression 9412 0.144931 0.185745 -0.053785    -0.009888        0.021020              0.030908
  HistGradientBoosting 9412 0.153697 0.198952 -0.208975    -0.009888       -0.011836             -0.001948
         Random Forest 9412 0.156935 0.203337 -0.262853    -0.009888       -0.020755             -0.010867

## Limitations
- The target is a 63-observation forward return, not necessarily exactly three calendar months.
- Predictor allowlisting reduces but does not eliminate the need to verify point-in-time feature construction.
- A lower MAE does not prove that a trading strategy is profitable after transaction costs and other constraints.
- All conclusions apply to this historical held-out period only.