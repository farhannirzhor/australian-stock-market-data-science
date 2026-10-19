# Phase 16 — Final Model Evaluation

## Selected model test metrics
- Model: Training mean baseline
- Test rows: 9412
- MAE: 0.143784
- RMSE: 0.184964
- R²: -0.044950
- Actual mean return: -0.009888
- Predicted mean return: 0.028474
- Mean prediction bias: 0.038362

## Validation comparison
Best validation MAE model: Training mean baseline (MAE=0.141984).

## Test comparison availability
Only the selected model's test predictions were found. Do not claim that every candidate model was compared on the test set.

## Baseline assessment
{
  "status": "could not identify both baseline and non-baseline rows",
  "rows_found": [
    {
      "model": "Train+validation mean baseline",
      "n": 9412,
      "mae": 0.143784486091985,
      "rmse": 0.1849644945838032,
      "r2": -0.0449496718904638,
      "actual_mean": -0.009887806217044,
      "predicted_mean": 0.0284744327304448,
      "mean_prediction_bias": 0.0383622389474888
    },
    {
      "model": "Training mean baseline",
      "n": 9412,
      "mae": 0.143784486091985,
      "rmse": 0.1849644945838032,
      "r2": -0.0449496718904638,
      "actual_mean": -0.009887806217044,
      "predicted_mean": 0.0284744327304448,
      "mean_prediction_bias": 0.0383622389474888
    }
  ]
}

## Limitations
- A regression score does not establish trading profitability.
- The selected-model prediction file alone cannot reconstruct predictions from models that were not saved.
- Features must be checked for point-in-time availability and target leakage.
- Results describe the historical test period only; they do not guarantee future performance.