# Model Card: D2C Churn Prediction Model v1.0

## 1. Intended Use
* **Primary Users:** Growth Marketing Teams, CRM Automation Workflows, and Customer Success Teams.
* **Intended Use Case:** Predicts the probability of individual customer churn over a 60-day window using features recorded before the snapshot date.
* **Out-of-Scope Uses:** Sub-second application behavior tracking or lifetime value estimations.

## 2. Training & Validation Set Data
* **Data Sources:** Core user attributes, purchase logs, support histories, and platform web logs.
* **Target Label Definition:** Complete absence of purchase actions within a 60-day post-snapshot target window.
* **Split Ratio:** 70% Train, 15% Validation, and 15% Test partitions split using unique customer IDs to prevent data leakage.

## 3. Metrics & Performance
* **Primary Metric:** Optimization focuses on F1-Score to balance budget waste with churn coverage.
* **Performance Matrix:**
  * Champion Random Forest F1: 0.79
  * Test Recall: 0.82 | Test Precision: 0.76

## 4. Limitations & Ethical Risks
* **Ethical Risks:** Direct incentive distributions can cause customer dissatisfaction if promotional distributions are viewed as unfair or biased.
* **Limitations:** Performance drops during holiday sales (e.g., Black Friday) due to high transactional variations.