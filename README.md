# Employee Attrition Prediction

Machine learning project focused on identifying employees at higher risk of leaving the organization and understanding the factors most associated with employee attrition.

The project uses **Logistic Regression**, class balancing with **SMOTE**, threshold optimization and model interpretation to support a more data-driven approach to employee retention.

## Overview

Employee attrition is an imbalanced classification problem: employees who leave typically represent a smaller portion of the workforce.

Rather than optimizing only for overall accuracy, this project places greater emphasis on **recall**, aiming to identify a larger share of employees who are actually at risk of leaving.

The workflow includes:

* Data preprocessing and feature encoding
* Train/test split
* Logistic Regression baseline
* Class balancing with SMOTE
* Decision threshold optimization
* Feature importance analysis
* Cross-validation
* Final model evaluation

## Methodology

### 1. Data Preparation

Categorical and numerical variables were prepared for modeling, and the dataset was divided into:

* **80% training data**
* **20% test data**

### 2. Baseline Model

A **Logistic Regression** model was trained as the initial classifier.

Performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score

### 3. Class Imbalance

Because attrition cases represent the minority class, **SMOTE (Synthetic Minority Oversampling Technique)** was applied to the training data.

The model was then retrained using the balanced dataset.

### 4. Threshold Optimization

The classification threshold was adjusted to improve **recall**, increasing the model's ability to identify employees who were likely to leave.

### 5. Model Interpretation

Logistic Regression coefficients were analyzed to identify variables with the strongest relationship with employee attrition.

### 6. Validation

A **5-fold cross-validation** strategy was used to evaluate the consistency of the model across different subsets of the data.

## Results

| Metric              |          Result |
| ------------------- | --------------: |
| Accuracy            |        **0.73** |
| F1-Score            |        **0.36** |
| Recall              |        **0.74** |
| Cross-validation F1 | **0.32 ± 0.03** |

The optimized model reached a **recall of 74%**, prioritizing the identification of employees at risk of attrition over maximizing overall accuracy.

## Key Attrition Factors

Among the variables with the strongest influence on the model were:

1. `OverTime_Yes`
2. `Department_Research & Development`
3. `Department_Sales`
4. `MaritalStatus_Married`
5. `YearsInCurrentRole`

These variables help illustrate how interpretable machine learning models can be used not only for prediction, but also to investigate patterns associated with employee turnover.

## Tech Stack

**Python**

* `pandas` — data manipulation
* `numpy` — numerical operations
* `scikit-learn` — preprocessing, modeling and evaluation
* `imbalanced-learn` — SMOTE and class balancing
* `matplotlib` — data visualization
* `seaborn` — exploratory visualization

## Repository

```text
HR-Predict/
├── HR_Analytics_Employee.ipynb
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
└── README.md
```

The complete analysis and modeling workflow is available in the Jupyter Notebook.

## Next Steps

Potential improvements include:

* Comparing Logistic Regression with **Random Forest** and **Gradient Boosting**
* Expanding feature engineering
* Testing alternative class-balancing strategies
* Evaluating probability calibration
* Comparing different decision thresholds based on business costs
* Adding explainability methods such as SHAP
* Translating model outputs into employee retention risk segments

## Business Perspective

In a real People Analytics environment, a model like this should not be used to make automatic employment decisions.

Its value is primarily as a **decision-support tool**, helping HR teams identify workforce patterns, investigate potential drivers of attrition and prioritize retention analyses.
