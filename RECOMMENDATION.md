# Production Model Recommendation Report - Week 2

## 1. Data Leakage Prevention Methodology
To ensure zero data leakage, missing value imputation and feature scaling parameters were computed **strictly on the training dataset** (`X_train`) and then applied to the validation and test datasets (`X_val` and `X_test`)[cite: 6].

## 2. Evaluation Metric Rationale
Given the high class imbalance (~8% default rate), **Accuracy** was discarded as a target metric[cite: 6]. **ROC-AUC** and **F1-Score / Recall** were prioritized to ensure maximum sensitivity in detecting potential default risks while balancing false alarms[cite: 6].

## 3. Production Recommendation
**Recommended Model:** LightGBM Classifier[cite: 6].
- **Performance:** LightGBM achieved the highest ROC-AUC score and better recall compared to Logistic Regression and Random Forest[cite: 6].
- **Interpretability:** Feature importance analysis revealed that external credit ratings (`EXT_SOURCE_2` and `EXT_SOURCE_3`) are the strongest predictors of default risk[cite: 6].
- **Efficiency:** LightGBM offers significantly faster training and inference times, making it ideal for real-time production deployment[cite: 6].
