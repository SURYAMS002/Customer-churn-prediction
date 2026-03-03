## Customer Churn Prediction Using Stacked Ensemble Learning

### 1. Project Overview

This project develops a robust and scalable machine learning framework for predicting customer churn in the telecom domain. The objective is to identify customers who are likely to discontinue services and to enable proactive retention strategies through data-driven insights.

The system integrates advanced ensemble learning techniques with model interpretability tools to deliver high predictive performance while maintaining transparency. In addition to churn prediction, a High-Value Customer scoring mechanism is introduced to prioritize retention efforts effectively.

---

### 2. Dataset Description

The dataset consists of structured telecom customer behavioral data collected over a 90-day period. It includes:

* Application usage metrics
* Voice call statistics
* Data consumption patterns
* Data pack recharges
* Value-added service activity
* Customer tenure and engagement features

Extensive feature engineering transforms daily usage logs into a high-dimensional structured dataset containing aggregated statistical indicators such as:

* Average and variance of data usage
* Frequency of recharges
* Peak usage behavior
* Service interaction intensity
* Activity trends over time

The final dataset contains over one thousand derived behavioral features.

---

### 3. Data Preprocessing

The preprocessing pipeline includes:

* Handling missing values
* Outlier detection and treatment
* Feature scaling and normalization
* Encoding categorical variables
* Addressing class imbalance

Since churn datasets are typically imbalanced, RandomUnderSampler is applied to balance churn and non-churn classes during training, improving model sensitivity to minority cases.

---

### 4. Modeling Approach

#### 4.1 Base Models

Multiple machine learning models are trained:

* XGBoost
* Gradient Boosting Classifier
* Logistic Regression

Each model captures different aspects of nonlinear and linear relationships in customer behavior.

---

#### 4.2 Stacked Ensemble Architecture

A Stacking Classifier is implemented where:

* XGBoost and Gradient Boosting act as base learners
* Logistic Regression serves as the meta-classifier

This ensemble structure improves generalization performance by combining the strengths of tree-based and linear models.

Cross-validation is used to prevent overfitting and ensure stable performance across folds.

---

### 5. Model Evaluation

Model performance is evaluated using classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

Results achieved:

* Accuracy: 97.6 percent
* Recall: 0.98
* Precision: 0.92
* ROC-AUC: 0.9915

The high recall ensures that potential churners are correctly identified, which is critical in retention-focused business environments.

---

### 6. Model Explainability

To ensure interpretability, SHAP (Shapley Additive Explanations) is integrated into the pipeline.

This enables:

* Global feature importance analysis
* Local prediction-level explanations
* Visualization of feature contribution toward churn probability

Key churn-driving factors identified include:

* Reduced data pack recharges
* Decrease in voice call frequency
* Lower engagement with popular applications
* Declining service usage patterns

This interpretability layer ensures the model is not a black-box system and supports business decision-making.

---

### 7. High-Value Customer Scoring System

Beyond churn prediction, a High-Value Customer (HVC) scoring mechanism is introduced.

The score combines:

* Predicted churn probability
* Normalized usage intensity
* Revenue-related behavioral indicators

Customers with high churn probability and high usage are prioritized for retention campaigns. This improves marketing ROI and resource allocation efficiency.

---

### 8. Visualization and Insights

The project includes:

* ROC curve visualization
* Confusion matrix analysis
* Feature importance plots
* SHAP summary plots
* Churn probability distribution analysis

These visual tools support strategic planning and stakeholder communication.

---

### 9. System Architecture

The pipeline follows a modular architecture:

1. Data ingestion
2. Preprocessing and feature engineering
3. Class balancing
4. Model training
5. Stacked ensemble construction
6. Evaluation
7. Explainability and scoring
8. Insight generation

This structure ensures scalability and production deployment readiness.

---

### 10. Technologies Used

* Python
* pandas and NumPy
* scikit-learn
* XGBoost
* imbalanced-learn
* SHAP
* Matplotlib and Seaborn

---

### 11. Conclusion

This project demonstrates how advanced ensemble learning combined with interpretability techniques can significantly improve churn prediction accuracy. The integration of High-Value Customer scoring transforms the model from a predictive tool into a strategic business intelligence system.

The framework can be extended to subscription-based businesses, SaaS platforms, fintech services, and other industries where customer retention is critical.
