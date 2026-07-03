# 💰 Loan Approval Prediction

A machine learning classification project that predicts whether a loan application will be **approved or rejected** based on applicant and financial details.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-150458?logo=pandas)
![scikit--learn](https://img.shields.io/badge/scikit--learn-ML%20Models-F7931E?logo=scikitlearn)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

---

## 📖 About

This project builds and evaluates classification models to predict loan approval status from the **LoanApprovalPrediction.csv** dataset. It covers data cleaning (handling missing values), categorical encoding, model training with **Logistic Regression**, and lays the groundwork for comparison against **Decision Tree** and **Random Forest** classifiers.

## 📊 Dataset

The dataset (`LoanApprovalPrediction.csv`) contains **598 records** and **13 columns**:

| Column | Type | Description |
|---|---|---|
| `Loan_ID` | object | Unique loan application ID (dropped before modeling) |
| `Gender` | object | Applicant gender |
| `Married` | object | Marital status |
| `Dependents` | float | Number of dependents |
| `Education` | object | Education level (graduate/not graduate) |
| `Self_Employed` | object | Self-employment status |
| `ApplicantIncome` | int | Applicant's income |
| `CoapplicantIncome` | float | Co-applicant's income |
| `LoanAmount` | float | Requested loan amount |
| `Loan_Amount_Term` | float | Loan repayment term (in months) |
| `Credit_History` | float | Whether credit history meets guidelines (1/0) |
| `Property_Area` | object | Urban / Semiurban / Rural |
| `Loan_Status` | object | Target variable — loan approved (Y/N) |

## ⚙️ Workflow

1. **Data Loading** — dataset read with `pandas`.
2. **Data Understanding** — inspected structure, types, and missing values with `data.info()`.
3. **Categorical Encoding** — `Gender`, `Married`, `Education`, `Self_Employed`, and `Property_Area` encoded to numeric form using `LabelEncoder`.
4. **Column Cleanup** — `Loan_ID` dropped (non-predictive identifier).
5. **Missing Value Handling**:
   - `Dependents` → filled with `0`
   - `LoanAmount` → filled with `1`
   - `Loan_Amount_Term` → filled with the column mode
   - `Credit_History` → filled with `0`
6. **Feature/Target Split** — all columns except `Loan_Status` used as features (`x`); `Loan_Status` as the target (`y`).
7. **Train/Test Split** — 80/20 split via `train_test_split` (`random_state=31`).
8. **Model Training** — `LogisticRegression` fit on the training data.
9. **Evaluation** — accuracy and confusion matrix computed on the test set.
10. **Further Algorithms (in progress)** — `DecisionTreeClassifier` and `RandomForestClassifier` set up for comparison.

## 🧠 Models

```python
from sklearn.linear_model import LogisticRegression
lrmodel = LogisticRegression()
lrmodel.fit(xtrain, ytrain)

# Additional models being explored:
from sklearn.tree import DecisionTreeClassifier
dtmodel = DecisionTreeClassifier(criterion='gini')

from sklearn.ensemble import RandomForestClassifier
rfmodel = RandomForestClassifier(max_depth=2, random_state=0)
```

> ⚠️ **Note:** `LogisticRegression` raised a `ConvergenceWarning` (lbfgs failed to converge within the default iteration limit). Increasing `max_iter` or scaling the features (e.g. `StandardScaler`) is recommended to resolve this.

## 📈 Results

| Metric | Value |
|---|---|
| Accuracy | **78.33%** |

**Confusion Matrix:**

| | Predicted: No | Predicted: Yes |
|---|---|---|
| **Actual: No** | 18 | 16 |
| **Actual: Yes** | 10 | 76 |

```python
from sklearn.metrics import accuracy_score, precision_score, confusion_matrix

print(accuracy_score(ytest, ypred) * 100)
print(confusion_matrix(ytest, ypred))
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas scikit-learn
```

### Run

1. Open the notebook in Jupyter or Google Colab.
2. Ensure `LoanApprovalPrediction.csv` is in the working directory (or upload it if using Colab).
3. Run all cells to preprocess the data, train the model(s), and view accuracy/confusion matrix results.

## 🧰 Tech Stack

- **Python**
- **Pandas** — data loading, cleaning, and manipulation
- **scikit-learn** — `LabelEncoder`, `train_test_split`, `LogisticRegression`, `DecisionTreeClassifier`, `RandomForestClassifier`, evaluation metrics

## 🔮 Possible Improvements

- Resolve the logistic regression convergence warning via feature scaling and/or a higher `max_iter`.
- Complete and evaluate the Decision Tree and Random Forest models for comparison.
- Address class imbalance if present (check distribution of `Loan_Status`).
- Add precision, recall, and F1-score alongside accuracy for a fuller picture.
- Cross-validation for more robust performance estimates.

## 👤 Author

**Duvvu Lakshmi Prasanna**
[GitHub](https://github.com/DuvvuLakshmiPrasanna)
