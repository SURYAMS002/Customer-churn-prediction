Here is a **medium-length, professional GitHub description** (balanced — not too long, not too short):

---

## 📊 Customer Churn Prediction & High-Value Customer Segmentation

This project develops an end-to-end **machine learning pipeline** to predict customer churn using 90-day telecom behavioral data (app usage, voice calls, data packs, and VAS activity). The system transforms daily usage logs into a high-dimensional feature matrix (1000+ features) and applies advanced ensemble modeling to achieve strong predictive performance.

To handle class imbalance, RandomUnderSampler is used before training a **Stacked Ensemble Model** combining:

* XGBoost
* Gradient Boosting
* Logistic Regression (Meta-Classifier)

The model achieves:

* **Accuracy:** 97.6%
* **Precision:** 0.92
* **Recall:** 0.98
* **ROC-AUC:** 0.9915

SHAP explainability is integrated to identify key churn-driving features such as YouTube usage, Facebook activity, data pack engagement, and voice usage patterns.

Beyond prediction, the project introduces a **High-Value Customer (HVC) scoring mechanism** that combines churn probability with normalized service usage to identify high-risk, high-revenue customers. Automated retention recommendations are generated to support targeted marketing and loyalty strategies.

Built using Python, pandas, scikit-learn, XGBoost, SHAP, and imbalanced-learn.

---

If you want, I can also give:

* 🔹 A resume version (5–6 lines impact-focused)
* 🔹 A recruiter-friendly version
* 🔹 A technical-heavy version for GitHub stars
