## Fraud Detection in Imbalanced Financial Transactions

###  Problem Overview

Financial fraud detection is a classical rare-event problem, where fraudulent transactions represent a small fraction of total operations (~3.5% in this dataset). In such scenarios, traditional metrics like accuracy become misleading, requiring a more risk-oriented evaluation focused on recall, precision, F1-score, and AUC.

This project develops and evaluates supervised machine learning models to detect fraudulent online transactions, with emphasis on class imbalance handling, robust validation, probability calibration, and decision threshold optimization.

### Dataset

* Source: IEEE-CIS Fraud Detection (Kaggle Competition)
* Observations: 590,540 transactions
* Fraud Rate: ~3.5%
* Features: Transaction amount, card information, behavioral signals, temporal attributes, and engineered risk-based features

Data was obtained via the official Kaggle API.

### Methodology

The analysis follows a structured risk modeling pipeline:

1. Business Framing & Risk Contextualization
* Rare-event classification
* Cost-sensitive evaluation perspective

2. Data Preparation & Risk-Oriented Cleaning
* Missing value handling
* Feature selection based on statistical relevance
* Feature engineering

3. Exploratory Risk Analysis
* Statistical testing (Mann-Whitney, Chi-Square)
* Extreme value behavior assessment
* Relative risk segmentation

4. Model Selection & Validation
* Logistic Regression (baseline & class-weighted)
* Random UnderSampling
* Balanced Random Forest
* Easy Ensemble
* Stratified K-Fold Cross-Validation

5. Probability Calibration
* Brier Score evaluation
* Calibration curve analysis

6. Decision Optimization
* Precision–Recall analysis
* Threshold comparison
* Operational trade-off assessment

### Key Results

* Selected Model: Balanced Random Forest
* ROC-AUC: ~0.91
* Recall (Fraud Class): ~0.79
* Optimized Threshold: 0.75
* Best F1-score: ~0.60

Cross-validation confirmed model stability, and threshold optimization allowed alignment between fraud detection performance and operational sustainability.

### Risk-Oriented Insights

* High recall significantly increases false positives.
* Higher thresholds improve precision but allow more fraud to pass undetected.
* Model performance must be evaluated under operational constraints.
* Decision thresholds should ideally incorporate explicit cost matrices.

This study demonstrates that fraud modeling is fundamentally a decision optimization problem under class imbalance, requiring integration of discrimination, calibration, and cost-sensitive evaluation.

### Technologies Used

* Python
* Pandas & NumPy
* Scikit-learn
* Imbalanced-learn
* Matplotlib / Seaborn

---

**Author:** Karen Pessoa
PhD Candidate in Statistics | Risk Modeling & Machine Learning


