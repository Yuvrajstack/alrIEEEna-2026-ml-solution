# alrIEEEna-2026-ml-solution
ML Arena 2026 – Fault Detection System


Problem Overview:
This project focuses on building a machine learning model to detect faulty devices based on numerical sensor measurements.

Each sample contains 47 features (F01–F47) representing device readings.
The goal is to classify whether a device is Normal (0) or Faulty (1).



Dataset Description:
Train.csv
47 numerical features (F01–F47)
Target column: Class
Test.csv
47 numerical features
ID column



Methodology/Approach:

1. The following steps were used to build the model:
2. Data preprocessing and feature selection
3. Separation of features and target variable
4. Implementation of Stratified 5-Fold Cross Validation
5. Training a LightGBM classifier for each fold
6. Generating Out-of-Fold (OOF) predictions
7. Optimizing the probability threshold using OOF predictions to maximize F1 score
8. Averaging predictions from all folds for final test predictions



Model Configuration:

Model: LightGBM
num_leaves = 96
min_child_samples = 30
learning_rate = 0.01
reg_alpha = 0.05
reg_lambda = 0.05
n_estimators = 5000


Evaluation:

Model performance was evaluated using F1 Score and Accuracy on cross-validation folds.

Example results:

F1 Score ≈ 0.987
Accuracy ≈ 0.990


Final Output:

Submission file format:
FINAL.csv
Columns:
ID, CLASS


Authors

Yuvraj Kabadwal
Vandana Bhandari
B.Tech Computer Science Engineering

