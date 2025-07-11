# 🧠 Disease Prediction Using Classification

**Author**: Wael Albakri  
**Course**: Bio Data Science  
**Date**: May 14, 2025  

## 📘 Introduction

This project explores how classification models can predict diseases using two very different datasets:

1. **Cancer gene expression dataset** with 12,750 features per patient (very high dimensional).
2. **Heart disease dataset** from UCI with 13 clinical features like age, cholesterol, etc.

The goal was to compare models including **K-Nearest Neighbors (KNN)**, **Decision Tree**, **Support Vector Machine (SVM)**, and **XGBoost**, and evaluate their performance using advanced metrics and visualizations.

---

## 📂 Data and Methods

### 📊 Datasets

- **Cancer Dataset**
  - 1,616 patients
  - 12,750 gene expression features
  - Labels: `0 = No Metastasis`, `1 = Metastasis`

- **Heart Disease Dataset (UCI)**
  - 1,025 samples
  - 13 features (e.g., chest pain, cholesterol)
  - Labels: `0 = No Disease`, `1 = Heart Disease`

### 🛠️ Tools & Libraries

- Python (Google Colab)
- Libraries: `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`, `xgboost`

### 🔍 Techniques

- Data Normalization with `StandardScaler`
- Dimensionality Reduction with `PCA`  
  - 300 components for Cancer  
  - 8 components for Heart
- 5-Fold Cross-Validation
- Evaluation Metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix, AUC Score
- Ensemble with `VotingClassifier`

---

## 📈 Results

### 🧬 Cancer Dataset

- **Decision Tree**: 
  - Correctly predicted 846 no-metastasis and 178 metastasis.
  - Misclassified: 315 false positives, 277 false negatives.
  - Struggled due to complexity and high-dimensional data.

- **KNN**: 
  - Performed better than Decision Tree.
  - Correct: 1,054 no-metastasis, 107 metastasis.
  - Still biased toward the majority class.

- **SVM**: 
  - Best accuracy: 1,103 no-metastasis, 61 metastasis.
  - Major issue: 394 metastasis cases misclassified.
  - Shows effect of imbalanced data.

📉 **Cancer AUC Score**: `0.6608`  
⚠️ Very imbalanced dataset → accuracy alone is misleading.

---

### ❤️ Heart Disease Dataset

- **Decision Tree**:  
  - 493/499 no-disease correct, 516/526 disease correct.
  - Very low error rate.

- **XGBoost**:  
  - Slightly better than Decision Tree.
  - 496/499 no-disease correct, 516/526 disease correct.
  - Best overall precision.

📈 **Heart AUC Score**: `0.9961`  
✅ Clean, balanced dataset → great model performance.

---

### 📊 Accuracy Summary

| Dataset      | Best Models        | Accuracy       |
|--------------|--------------------|----------------|
| Cancer       | SVM, KNN           | ~72%           |
| Heart        | Decision Tree, XGBoost | >98%       |

---

## 💬 Discussion

- Cancer dataset was more difficult due to class imbalance and high dimensions.
- Heart dataset had cleaner and more balanced data.
- VotingClassifier boosted F1-scores by combining model strengths.
- Confusion matrices helped understand which class was being misclassified.
- Decision Tree visualization was helpful to understand model logic.

---

## ✅ Conclusion

This project improved my understanding of:

- When and how to use cross-validation
- Importance of PCA for dimensionality reduction
- Why AUC is more informative for imbalanced data
- How visualization aids interpretation
- How to choose models based on data complexity

📌 It was a **solo project**, and all code and analysis were completed independently.

---

## 📁 Files in This Repo

- `Final_Project_Wael_Albakri.ipynb` – Jupyter Notebook with code and outputs  
- `Disease_Prediction_Dashboard.pbix` – Power BI Dashboard  
- `Final Project Report - Wael Albakri.pdf` – Full written report  

---

## 📊 Power BI Dashboard

For data presentation, a Power BI dashboard was also created to visually explore the data and model results in an interactive format.

---

## 🔗 How to Run

Simply download the Jupyter notebook file (`Final_Project_Wael_Albakri.ipynb`) and open it in Google Colab or JupyterLab.

All results, visualizations, and analysis are already included — no setup or data upload needed. Just scroll through and enjoy!

---

## 📬 Contact

If you have any questions or feedback about this project, feel free to reach out via GitHub or connect with me on LinkedIn.

Thanks for checking out my project!
