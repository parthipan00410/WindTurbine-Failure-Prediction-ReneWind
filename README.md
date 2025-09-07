# WindTurbine-Failure-Prediction-ReneWind
Artificial Neural Network (ANN) model for predicting wind turbine generator failures (predictive maintenance).

## Project Overview
This project develops an Artificial Neural Network (ANN) to predict wind turbine generator failures using confidential sensor data provided by ReneWind. The goal is to enable predictive maintenance by detecting failures early, thereby reducing costly replacements and optimizing repair/inspection schedules.
## Problem Statement
- Failures (1) → Generator breakdowns that require repair/replacement.
- No Failures (0) → Normal functioning.
- Cost hierarchy:
  - Replacement (most expensive)
  - Repair (moderate cost)
  - Inspection (least cost)
- Minimizing false negatives (missed failures) is critical, since missed detections lead to high replacement costs.
## Dataset
- Source: ReneWind (ciphered sensor data)
- Training set: 20,000 observations
- Test set: 5,000 observations
- Features: 40 predictors from turbine sensors
- Target variable:
  - 1 → Failure
  - 0 → No failure
## Approach
- Data Preprocessing
  - Normalized features
  - Handled class imbalance (if applied, e.g., oversampling/undersampling)
- Modeling
  - Built an Artificial Neural Network (ANN)
  - Tuned hyperparameters (layers, neurons, activation functions, learning rate, epochs, batch size)
- Evaluation Metric Priority
  - Recall → to reduce false negatives (missed failures)
  - Also reported Precision, Accuracy, F1-score
## Results
  - Metric	Training	Validation	Test
  - Recall	  0.89%	     0.91%	  0.85%
  - Precision	0.85%	     0.90%	  0.89%
  - F1-score	0.88%	     0.90%	  0.87%
  - Accuracy	0.98%	     0.99%	  0.98%
- Final model prioritized Recall = 0.85% (Test set), ensuring failures are detected early.
- Balanced with F1-score = 0.87% for overall robustness.
