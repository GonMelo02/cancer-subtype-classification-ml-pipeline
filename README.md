# Cancer Subtype Classification — Machine Learning on High-Dimensional Data

This project applies both **unsupervised and supervised machine learning** methods to classify molecular subtypes of glioblastoma multiforme (GBM) based on **gene expression data**.  
Although the dataset comes from a biomedical context, the focus of the project is on **handling high-dimensional data, model development, and evaluation**, making it relevant to general data science and machine learning domains.

---

##  Project Overview

The project was divided into two main parts: unsupervised exploration and supervised classification.

### **1. Unsupervised Learning**

Explored the structure of the data using multiple clustering and dimensionality reduction techniques to understand whether natural groupings align with known labels.

**Approaches tested:**
- **Feature selection:** Variance-based filtering  
- **Dimensionality reduction:** PCA, UMAP  
- **Clustering algorithms:** K-Means, Hierarchical Clustering  

**Evaluation methods:**
- Internal validation: Silhouette Score, Calinski–Harabasz Index, Davies–Bouldin Index  
- External validation: Adjusted Rand Index (ARI), Normalized Mutual Information (NMI)

This stage revealed that while some clustering approaches achieved good structural separation, the natural groupings did not fully match the known cancer subtypes — a common challenge in complex, overlapping data.

---

### **2. Supervised Learning**

Developed a **binary classification pipeline** to predict cancer subtypes (Classical vs Mesenchymal) using cross-validated machine learning workflows.

**Pipeline summary:**
- **Data splitting:** Stratified 5-Fold Cross-Validation  
- **Preprocessing:** Feature scaling with StandardScaler  
- **Feature selection:** ANOVA F-test (with the top 500 features)  
- **Model training:** Logistic Regression, SVM, Naive Bayes, Random Forest, XGBoost  
- **Model evaluation:** Accuracy, Precision, Recall, and F1-score (mean across folds)

The supervised stage demonstrated how different algorithms behave under high-dimensional and low-sample conditions, emphasizing the importance of robust preprocessing, feature selection, and model validation.

---

## Tools and Libraries

- **Python**  
- **scikit-learn**, **xgboost**  
- **pandas**, **numpy**, **matplotlib**, **seaborn**  
- **PCA**, **UMAP**, **K-Means**, **Hierarchical Clustering**

---

## Key Takeaways

- Illustrated a full ML workflow from **data preprocessing to model evaluation**.  
- Demonstrated the integration of **unsupervised exploration and supervised prediction**.  
- Highlighted challenges of **high-dimensional, small-sample datasets**.  
- Reinforced experience with **feature selection, dimensionality reduction, and validation techniques**.  

---

## 📁 Repository Structure

