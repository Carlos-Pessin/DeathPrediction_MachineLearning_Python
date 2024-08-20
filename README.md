Post-graduate project from Machine Learning applied to Medical Signals and Images at University of São Paulo
-----------
# WiDS challenge
Stanford University has lauched the WiDS (Women in Data Science) challenge in 2020, where the participants should propose a model to predict deaths in ICU units.
# Database
Global Open Source Severity of Illness Score (GOSSIS)  - Massachusetts Institute of Technology (MIT)
- 91.713 pacients
  - 83.781 lived (91,4%)
  - 7.907 died (8,6%)
- 147 ICU's
- 185 features for each pacient:
  - 16 demografic
  - 76 lab results
  - 52 vital signs
  - 41 severity scores
# LIBRARIES
- Pandas
- SKLearn
- Tensorflow/Keras
- Numpy
# DATA PREPARATION
## Data cleaning
- Features with 20% or more blank data was removed - 46% removed
- Pacientes with 20% or more blank data was removed - 8% removed
- Outliers were identified and removed for each feature - less than 1% of patients removed
## Data imputation
- For categorical data was created a "blank" category
- For numerical data, data was generated through a normal distribuition based on the feature itself
## Normalization
- Values were normalizated (0-1)
## Balancing classes
- Random subsample of 10% of living patients, to avoid interference - 
# MODELING
- Data split: 90% train / 10% test
## Feature selection
- PCA transformation - 45 components removed with less than 5% variance loss
- ICA transformation
- Random forest - feature importance parameter
- Final database 19407 patients and 40 features
## Classifier testing
- SVM classifier - rbf, sigmoid and poly kernels
- Random Forest classifier
- Hybrid SVM/RF classifier
# EVALUATION
- K-fold method - 10 folds randomized
## Metrics
- Accuracy
- Sensitivity
- Specificity
- AUC-ROC
# FINAL RESULTS
- Random forest was the best classifier
## Test results
- Accuracy: 75.6%
- Sensitivity: 81.9%
- Specificity: 75.0%
- AUC-ROC: 0.78
