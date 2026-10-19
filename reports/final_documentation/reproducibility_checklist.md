# Reproducibility Checklist

- [ ] Use the same Python environment and record package versions.
- [ ] Keep the original workbook unchanged and retain the generated raw/processed datasets.
- [ ] Run notebooks in phase order, beginning with data understanding and cleaning.
- [ ] Confirm all output paths and dataset versions before running downstream notebooks.
- [ ] Inspect each phase summary and audit warnings rather than relying only on successful cell execution.
- [ ] For final evaluation, select models on validation data and use the test set only for the final report.
- [ ] Do not claim investment profitability from historical regression metrics.