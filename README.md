# Healthcare 30-Day Readmission Prediction

## Project Overview

This project analyzes healthcare patient data to investigate factors associated with 30-day hospital readmission and evaluate machine learning models for predicting readmission risk.

## Objective

The main objectives are to:

- Explore patient characteristics associated with readmission.
- Analyze differences in readmission rates across patient and discharge characteristics.
- Develop baseline machine learning models.
- Evaluate model performance using metrics appropriate for an imbalanced classification problem.
- Identify limitations and opportunities for future improvement.

## Dataset

The dataset contains 30,000 patient records and 14 variables covering demographic, clinical, medication, hospitalization, and discharge information.

### Target Variable

`readmitted_30_days`

- No: 26,326 patients
- Yes: 3,674 patients

The target is imbalanced, with approximately 12.25% of patients experiencing readmission within 30 days.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Google Colab

## Methodology

1. Data inspection and quality checking
2. Exploratory data analysis
3. Target-variable analysis
4. Train-test split
5. Categorical feature encoding
6. Feature scaling
7. Logistic Regression
8. Random Forest
9. XGBoost
10. Class-imbalance handling
11. Feature importance analysis
12. Model evaluation

## Key Findings

Discharge destination showed one of the clearest descriptive differences in readmission rates:

| Discharge Destination | Readmission Rate |
|---|---:|
| Rehab | 17.50% |
| Nursing Facility | 16.85% |
| Home | 10.04% |

Length of stay showed relatively little variation in readmission rates, suggesting that it was not a strong standalone differentiating variable in this dataset.

## Model Results

The models demonstrated limited predictive performance.

| Model | Accuracy | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|
| Logistic Regression | 57.97% | 43.40% | 20.19% | 0.529 |
| Random Forest | 87.75% | 0% | 0% | 0.562 |
| XGBoost | 87.75% | 0% | 0% | 0.569 |
| Balanced XGBoost | 71.23% | 37.28% | 24.10% | 0.570 |

## Conclusion

The available variables demonstrated limited predictive power for individual 30-day readmission risk. Class weighting improved detection of the minority class but did not substantially improve overall discrimination.

The results highlight the importance of evaluating healthcare classification models using recall, precision, F1-score, and ROC-AUC rather than accuracy alone.

## Future Work

Future improvements could include:

- Additional clinical variables
- Previous admission history
- Comorbidity information
- Laboratory results
- Emergency department visits
- Medication changes
- Post-discharge follow-up information
- Feature engineering
- Hyperparameter tuning
- Threshold optimization
