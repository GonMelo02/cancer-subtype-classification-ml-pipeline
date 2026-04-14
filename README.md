# Cancer Subtype Classification — GBM Gene Expression

Binary classification of Glioblastoma Multiforme (GBM) molecular 
subtypes (Classical vs Mesenchymal) from high-dimensional gene 
expression data (5000 features, low-sample regime).

## Results (5-Fold Stratified Cross-Validation)

| Model | Accuracy | F1 |
|-------|----------|----|
| **SVM (RBF)** | **0.927 ± 0.034** | **0.927 ± 0.034** |
| Random Forest | 0.924 ± 0.034 | 0.924 ± 0.034 |
| Logistic Regression | 0.911 ± 0.034 | 0.911 ± 0.034 |
| Naive Bayes | 0.907 ± 0.036 | 0.907 ± 0.036 |
| XGBoost | 0.897 ± 0.036 | 0.897 ± 0.036 |

Best model: SVM with RBF kernel (accuracy 0.927).

## Pipeline
- Variance filtering + ANOVA F-test (top 500 features)
- StandardScaler inside cross-validation folds (no leakage)
- Stratified 5-Fold CV with GridSearchCV per model
- Unsupervised exploration: PCA, UMAP, K-Means, 
  Hierarchical Clustering

## Stack
Python · scikit-learn · xgboost · umap-learn · 
pandas · matplotlib · seaborn

## Run locally
pip install -r requirements.txt
jupyter notebook cancer_subtype_classification.ipynb

