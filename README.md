# CreditWise: Loan Approval Prediction & Financial Risk Analysis

A machine learning project designed to predict loan approval status and evaluate financial default risk. This project benchmarks multiple classification algorithms using real-world financial metrics, focusing on the trade-off between **Precision** and **Recall** in credit risk assessment.

---

## 📌 Project Overview

When evaluating loan applications, relying solely on **Accuracy** can lead to misleading conclusions due to class imbalance and the asymmetrical costs of financial errors:
* **False Positives (Precision risk):** Approving a high-risk applicant who defaults on the loan.
* **False Negatives (Recall risk):** Rejecting a creditworthy applicant, resulting in lost business.

This project implements an end-to-end Machine Learning pipeline to handle missing values, perform feature scaling, train multiple classifiers, and evaluate model performance beyond surface-level accuracy.

---

## 📊 Dataset Overview

The dataset (`loan_approval_data.csv`) contains **1,000 applicant records** across **20 feature attributes**:

* **Applicant Demographics:** Age, Gender, Education Level, Marital Status, Employment Status, Employer Category.
* **Financial Attributes:** Applicant Income, Co-applicant Income, Credit Score, Existing Debt, Savings, Collateral Value.
* **Loan Details:** Loan Amount, Loan Term, Loan Purpose, Property Area.
* **Target Variable:** `Loan_Approved` (Binary: `1` for Approved, `0` for Rejected).

---

## 🛠️ Project Workflow

1. **Exploratory Data Analysis (EDA):**
   * Visualised target class distribution and identified missing value patterns across numerical and categorical features.
2. **Data Cleaning & Imputation:**
   * Imputed missing numerical values using mean strategy via `SimpleImputer`.
   * Imputed missing categorical attributes using mode (`most_frequent`) strategy.
3. **Feature Preprocessing & Scaling:**
   * Standardised numerical variables using `StandardScaler` to optimize distance-based and gradient-based algorithms.
   * Encoded categorical attributes into machine-readable numeric formats.
4. **Model Training & Evaluation:**
   * Evaluated algorithms on an 80/20 train-test split using Accuracy, Precision, Recall, F1-Score, and Confusion Matrices.

---

## 📈 Model Performance & Comparison

| Model | Accuracy | Precision | Recall | F1-Score | Status |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | **87.0%** | **77.8%** | **80.3%** | **79.0%** | 🏆 **Best Performer** |
| **Gaussian Naive Bayes** | 86.5% | 80.4% | 73.8% | 76.9% | Strong Precision |
| **K-Nearest Neighbours (k=5)** | 76.5% | 63.0% | 55.7% | 59.1% | Baseline |

### Key Takeaway
* **Logistic Regression** achieved the best overall balance. Its **80.3% Recall** ensures that the majority of risky applications/defaulters are caught, while maintaining a competitive **77.8% Precision** to avoid excessive rejection of qualified applicants.
* **Naive Bayes** achieved slightly higher precision (80.4%), but dropped significantly in recall (73.8%), making it less effective at risk mitigation.

---

## 💻 Tech Stack & Libraries

* **Language:** Python 3.x
* **Data Processing:** Pandas, NumPy
* **Data Visualisation:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (`LogisticRegression`, `GaussianNB`, `KNeighborsClassifier`, `SimpleImputer`, `StandardScaler`, `train_test_split`)

---

## 🚀 How to Run locally

### 1. Clone the Repository
```bash
git clone https://github.com/maivee-rahman/Creditwise_Loan_Permission.git
cd Creditwise_Loan_Permission