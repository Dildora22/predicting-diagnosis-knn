# predicting-diagnosis-knn
Diabetes Prediction using K-Nearest Neighbors (KNN)

# Diabetes Prediction using K-Nearest Neighbors (KNN)

## Project Description
This project aims to predict diabetes in patients using the Pima Indians Diabetes dataset. The main goal is to identify diabetic patients correctly while minimizing false negatives, as missing a positive case can be dangerous in medical diagnosis.

## Dataset
- Size: 768 rows × 9 columns
- Target: Outcome (0 = non-diabetic, 1 = diabetic)
- Features: Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age

## Data Preprocessing
- Checked for missing or invalid values using .describe() and counted zeros.
- Zero values in physiological features (Glucose, BloodPressure, SkinThickness, Insulin, BMI) were replaced with median values.
- **Pregnancies zeros were retained**, as they represent valid cases of women with no prior pregnancies.
- ApplStandardScalerer** to scale all features.

## ModeAlgorithm:m:** K-Nearest Neighbors (KNNHyperparameter tuning:g:** Used GridSearchCV to select the best n_neighbors (odd numbers from 3 to 30) wrecall as the scoring metricic**Train/Test split:t:** 80/20  and random_state=42.
**Best parameters found:**

Key takeaway: The model reduced false negatives significantly compared to the initial baseline, which is critical for medical diagnosis.

## Insights
- Treating zeroes as missing values improved recall for diabetic patients.
- GridSearchCV helped find the optimal number of neighbors (k=11).

## Next Steps
- Threshold tuning to further increase recall
- Comparison with other models (Logistic Regression, RandomForest)
- Feature importance analysis
