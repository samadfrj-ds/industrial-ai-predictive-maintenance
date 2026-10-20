# Phase 04 – Anomaly Detection Evaluation

## Objective

Evaluate the existing residual-based Linear Regression
baseline on multiple wind turbine events without retraining
the model or modifying the anomaly threshold.

## Methodology

- Dataset: CARE to Compare, Wind Farm A
- Training asset: Asset 0
- Evaluation assets: Asset 0 and Asset 10
- Model: Linear Regression
- Anomaly score: Actual temperature - Predicted temperature
- Alert threshold: Original Phase 03 training-based threshold
- Evaluation filtering: Generator speed > 0 and complete model values
- No retrospective status label filtering
- Nominal evaluation window: 48 hours

## Key Findings

### Same-Asset Evaluation

- Two evaluable anomaly events produced alerts.
- Event 0: 15 alerts; first observed lead time 36.50 hours.
- Event 73: 30 alerts; first observed lead time 44.17 hours.
- Event 26: Not evaluable due to unavailable pre-event prediction data.
- Both selected 48-hour normal windows produced zero alerts.

### Extended Normal Operation

- Event 24: 3 alerts in 2 alarm groups.
- Event 71: 0 alerts.
- Combined alarm frequency: 0.075 groups per 24 valid
  observation hours.

### Cross-Asset Evaluation

- Normal Events 3 and 17: No alerts.
- Generator bearing failure Event 40: No alerts.
- Event 40 provides only 24 hours of pre-event data.
- Cross-asset early-warning capability was not demonstrated.

## Limitations

- Small and non-representative event sample.
- Exploratory event selection and evaluation.
- Unequal pre-event data availability.
- Possible differences in operating conditions.
- Temporal gaps caused by excluded operating observations.
- Potential prediction bias and limited model transferability.
- Retrospective event annotations do not establish physical
  fault onset times.
- No independently calibrated anomaly threshold.
- Observed detection rates do not establish generalization
  performance or reliable early-warning capability.

## Conclusion

The baseline identified elevated temperature residuals before
two documented events on the training asset.

However, it failed to flag the evaluated bearing failure
on Asset 10.

The results support further systematic evaluation and
model development, but do not demonstrate reliable
predictive maintenance performance.
