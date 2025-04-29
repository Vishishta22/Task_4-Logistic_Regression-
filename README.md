# Task_4-Logistic_Regression-
Objective
The aim of this project is to build a binary classification model using Logistic Regression to predict whether water is potable (drinkable) based on its physicochemical properties.

Tools & Libraries Used
Python

Pandas

Scikit-learn

Matplotlib & Seaborn (for visualization)

Dataset Overview
Dataset: water_potability.csv

Target Column: Potability

0 → Not potable

1 → Potable

Features:

ph

Hardness

Solids

Chloramines

Sulfate

Conductivity

Organic_carbon

Trihalomethanes

Turbidity

Data Preprocessing
Missing rows has been removed using dropna()

Features were standardized (z-score normalization) using StandardScaler.

Train-test split was done using an 80/20 split with stratify to preserve class distribution.
Model Training
A Logistic Regression model was trained using the training dataset. The model was then evaluated using common classification metrics: confusion matrix, precision, recall, and ROC-AUC.
Coefficients:

0.038, -0.014,  0.084,  0.035, -0.044, -0.064,  0.026,  0.0037, 0.035 

Each coefficient reflects the strength and direction of the relationship between a feature and potability.

Intercept:

-0.3948

Precision: 0.41

Precision tells us that 41% of the samples predicted as potable were actually potable.

Recall: 0.48

Recall indicates that 48% of the true potable samples were successfully identified by the model.

Threshold Tuning

The decision threshold for the classifier was adjusted from the default value of 0.5 to 0.3 to optimize recall and precision. By adjusting the threshold, we can balance between false positives and false negatives.

Threshold = 0.3

A custom threshold was applied to improve recall.

Confusion Matrix:

After tuning the threshold to 0.3, the confusion matrix showed:

[[  0 240]

 [  0 163]]

This indicates that the model is predicting many non-potable samples as potable (false positives), but it does not miss any potable samples (no false negatives).

Sigmoid Function Explanation

The logistic regression model uses the sigmoid function to predict probabilities. The function converts a linear combination of input features into a probability score between 0 and 1, which is used for binary classification.

Requirements

To run this project, you need to install the following Python libraries:

pandas: for data manipulation

numpy: for numerical operations

matplotlib: for plotting graphs

scikit-learn: for building the logistic regression model and evaluation
