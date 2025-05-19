# PCOS Detection Using Machine Learning

This project explores the application of various machine learning models to detect Polycystic Ovary Syndrome (PCOS) using laboratory blood test data.

## 📌 Project Objectives

- Analyze PCOS-related lab test data.
- Preprocess data: handle missing values, standardize features, encode categorical variables.
- Extract key features that significantly impact PCOS diagnosis.
- Train and evaluate machine learning models for accurate classification.
- Compare models based on accuracy, precision, recall, and F1-score.

## 🧪 Dataset

- **Source:** Public dataset certified by Johns Hopkins Medicine.
- **Shape:** 541 samples, 44 features (both continuous and categorical).
- **Label:** `PCOS (Y/N)` encoded as 1 (positive), 0 (negative).

## 🔍 Methods

- **Preprocessing:** Handling missing values, feature normalization, categorical encoding.
- **Exploratory Analysis:** Histograms, box plots, heatmaps, and VIF for multicollinearity check.
- **Feature Selection:** LassoCV used to identify most relevant features.
- **Models Used:**
  - Decision Tree
  - Random Forest
  - Logistic Regression
  - LDA / QDA
  - K-Nearest Neighbor (KNN)
  - Support Vector Machine (SVM)
  - Gaussian Naive Bayes
  - Gradient Boosting

## 📊 Results

| Model              | Accuracy | F1-Score | Precision | Recall |
|-------------------|----------|----------|-----------|--------|
| Decision Tree      | 0.8241   | 0.6667   | 0.6786    | 0.6552 |
| Random Forest      | 0.8519   | 0.7143   | 0.7407    | 0.6897 |
| Logistic Regression| 0.8519   | 0.7143   | 0.7407    | 0.6897 |
| SVM                | 0.8704   | 0.7500   | 0.7778    | 0.7241 |
| KNN                | **0.8796** | **0.7547** | **0.8333** | 0.6897 |
| GaussianNB         | 0.7870   | 0.6900   | 0.5652    | **0.8966** |
| Gradient Boosting  | 0.8519   | 0.7037   | 0.7600    | 0.6552 |

> **Note:** KNN achieved the highest overall accuracy, while GaussianNB had the best recall.

## ✅ Key Findings

- KNN and SVM performed best in terms of balanced performance.
- Age and follicle count (L & R) were strong indicators of PCOS.
- Features like BMI, weight, and blood group were less relevant based on Lasso regression.


## 📌 Dependencies

- Python (3.8+)
- NumPy, Pandas
- scikit-learn
- Seaborn, Matplotlib

Install with:
```bash
pip install -r requirements.txt


We hope you find this repository valuable and engaging as you explore the fascinating world of machine learning. Happy learning and coding!
