# Day 05 — Hyperparameter tuning (detailed walkthrough)

Day 05 focuses on **systematic model improvement** through hyperparameter tuning.
Instead of guessing settings manually, this notebook uses a reproducible workflow with cross-validation and model selection tools.

## What this project shows

- Clear explanation of **parameters vs hyperparameters**
- Proper **train/test separation** to avoid leakage
- **Stratified k-fold cross-validation** for robust tuning
- Full **GridSearchCV** workflow (exhaustive search)
- Full **RandomizedSearchCV** workflow (efficient sampling)
- Baseline vs tuned model comparison using multiple metrics:
  - Accuracy
  - Precision
  - Recall
  - F1
  - ROC-AUC

## Why this day matters

Hyperparameter tuning is where many models move from “works” to “production-ready.”
This day also builds the bridge between:

- **Day 02/03** model building + evaluation
- **Day 06** interpretability and explanation of tuned models

## Folder layout

```text
.
├── notebook.ipynb
└── README.md
```

## How I run it

1. Install dependencies:
   ```bash
   pip install numpy pandas scikit-learn
   ```
2. Open the notebook and run all cells in order.

## Notebook flow

1. Theory recap (hyperparameters + cross-validation)
2. Dataset loading and stratified split
3. Baseline logistic regression pipeline
4. Grid search tuning and result inspection
5. Randomized search tuning and result inspection
6. Final model comparison + practical selection framework
7. Day summary and handoff to interpretability

## Notes (written by me)

- I intentionally tune a familiar dataset so improvements are easier to interpret.
- I use `Pipeline` everywhere to keep preprocessing and modeling consistent.
- I evaluate with more than accuracy, because single-metric decisions can hide failure modes.
