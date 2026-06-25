---
noteId: "5debf770708611f19ec49d9bd6d884a1"
tags: []

---

# Credit Risk Prediction and Loan Approval Analytics

This repository contains a completed analytics notebook for studying loan approval outcomes with a credit-risk lens. The notebook is written as a practical research report with careful interpretation of what the dataset can and cannot prove.

## What This Notebook Covers

- Dataset loading from a local CSV
- Data quality and missing-value audit
- Descriptive statistics by approval outcome
- Exploratory visual analytics for credit history, income, loan amount, education, and property area
- Statistical testing for numeric and categorical variables
- Correlation and VIF review for multicollinearity
- VADER sentiment applicability audit
- Regularized logistic regression with grid search
- Confusion matrix, ROC curve, precision-recall curve, cross-validation, and threshold tradeoff analysis
- Coefficient review for model interpretability

## Main Result

Credit history is the strongest visible signal for loan approval in this dataset. Income, coapplicant income, and loan amount add context, but they should not be interpreted as independent explanations without considering missing values, engineered-feature overlap, and the dataset's approval-status target.

## Important Note

This dataset records `Loan_Status`, not verified repayment or default behavior. The notebook therefore frames the target as approved / lower risk versus not approved / higher risk instead of making unsupported claims about actual default.

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/02_credit_risk_prediction.ipynb
```

The notebook expects this file:

```text
data/raw/train_u6lujuX_CVtuZ9i.csv
```

Exported charts are saved in `outputs/figures/`.
