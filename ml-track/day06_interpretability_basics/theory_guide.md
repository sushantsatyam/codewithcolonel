# Day 06 — Interpretability basics (theory guide)

## Goal

Interpretability helps you understand **why** a model makes certain predictions. This notebook focuses on two practical techniques that work well for tabular models.

## Feature importance (built-in)

Tree-based models (like Random Forests) expose `feature_importances_` based on how much each feature reduces impurity across the ensemble.

**Pros**
- Fast and easy to compute.
- Good first pass for understanding model behavior.

**Cons**
- Can be biased toward high-cardinality or correlated features.
- Reflects training data, not necessarily generalization behavior.

## Permutation importance

Permutation importance measures how much model performance drops when you **shuffle** one feature at a time.

**Pros**
- Model-agnostic and closer to the model’s actual predictive reliance.
- More robust for comparing features.

**Cons**
- More expensive to compute.
- Can still be affected by correlated features.

## Reading the results

- Look for features that appear in both importance lists.
- Treat sudden disagreements as a **signal to investigate**.
- Validate with domain knowledge (not just the metric).

## Open data notes

We use the **Iris** dataset to show the workflow on a familiar, open dataset.

## Extension ideas

- Add SHAP values for local explanations.
- Compare importances across multiple models.
- Use cross-validation to confirm stability.
