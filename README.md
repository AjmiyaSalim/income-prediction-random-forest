#  Income Prediction using Random Forest Classifier

##  Objective
The goal of this project is to build a machine learning model that predicts whether an individual's income exceeds \$50K per year using demographic and work-related attributes. The focus is on improving the detection of high-income individuals despite the dataset's class imbalance.

---

##  Introduction
Income classification is a common real-world problem with applications in targeted marketing, financial screening, and policy analysis. The dataset used here comes from the UCI repository and reflects real U.S. Census data, making it ideal for testing supervised classification models.

---

##  Dataset Overview

The dataset used in this project is referenced from the following Kaggle source:

🔗 [Adult Income Dataset – Kaggle](https://www.kaggle.com/code/prashant111/random-forest-classifier-feature-importance/input)

> **Note:** The dataset is not uploaded to this repository due to Kaggle’s usage policy. Please download it from the above link.

---

##  Why Random Forest?
Random Forest is a powerful ensemble learning method that builds multiple decision trees and combines their results. It was chosen for this project because it:
- Is resistant to overfitting
- Works well with missing or noisy data
- Automatically calculates feature importance
- Supports balancing classes with built-in options like `class_weight='balanced'`

---

##  Why We Didn't Use Feature Selection
Feature selection was skipped because:
- Random Forest inherently handles irrelevant features using random feature sampling.
- The model is already efficient and interpretable with a moderate number of features.
- Feature importance scores can be extracted **after training** for further analysis.

 In high-dimensional datasets (e.g., with hundreds of features), feature selection becomes more valuable for:
- Improving training speed
- Enhancing interpretability
- Reducing risk of overfitting

---

## Model Approach
- Algorithm: **RandomForestClassifier** from `sklearn.ensemble`
- Key Parameters:
  - `n_estimators`
  - `max_depth`
  - `criterion='gini'`
  - `class_weight='balanced'`
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

---

##  Results

The model generalizes well and performs strongly on imbalanced data — especially in capturing high-income predictions without excessive false negatives.

---

##  Conclusion
This project demonstrates that a balanced Random Forest classifier can effectively handle imbalanced income data and deliver reliable predictions. Its ability to catch most high-income individuals makes it useful in real-world tasks like credit scoring, income estimation, or resource planning.


