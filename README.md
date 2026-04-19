# Student stress classifier

Machine learning pipeline to classify stress levels in university students using Random Forest and SHAP explainability, based on a Kaggle survey dataset with 843 observations.

## Research question

*Which factors most influence stress levels among university students, and can they be predicted from self-reported behavioral and health indicators?*

## Approach

1. **Data cleaning** — missing values, duplicates, dummy encoding for categorical variables
2. **Target variable** — `stress_level` (0 = no stress, 1 = eustress, 2 = distress)
3. **Model** — Random Forest classifier with cross-validation
4. **Evaluation** — accuracy, confusion matrix, ROC/AUC
5. **Explainability** — SHAP values for global and local feature importance

## Key results

- Random Forest outperforms baseline on held-out test set
- Top predictors identified via SHAP: anxiety level, self-esteem, academic workload, social support
- SHAP force plots show individual-level explanations for model decisions
- Dataset of 843 students aged 18–21, Likert scale responses (1–5)

## Data

- Source: [Student Stress Monitoring Datasets — Kaggle](https://www.kaggle.com/datasets/mdsultanulislamovi/student-stress-monitoring-datasets)
- Observations: 843 university students
- Features: emotional, physical, and academic stress indicators
- Scale: 5-point Likert

## Stack

Python · scikit-learn · SHAP · pandas · matplotlib · seaborn

## Structure

```
├── AlexisCanez_ProjetoFinal_3.ipynb    ← main notebook
└── README.md
```

## How to run

```bash
pip install scikit-learn shap pandas matplotlib seaborn kaggle
jupyter notebook AlexisCanez_ProjetoFinal_3.ipynb
```
