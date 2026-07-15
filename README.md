# 🌱 Crop Recommendation System using Decision Tree

## 📌 Project Overview

This project develops a **Decision Tree Classifier** to recommend the most suitable crop based on soil nutrients and environmental conditions. The model follows a complete machine learning workflow, including data preprocessing, exploratory data analysis (EDA), outlier investigation, model training, hyperparameter tuning, and evaluation.

The goal is to help farmers make **data-driven crop selection decisions**, improving agricultural productivity and promoting sustainable farming practices.

---

## 🎯 Problem Statement

Selecting the right crop is crucial for maximizing yield and minimizing resource wastage. Traditional crop selection often depends on experience, whereas machine learning can provide accurate recommendations based on soil and climatic conditions.

This project predicts the most suitable crop using:

- Nitrogen (N)
- Phosphorus (P)
- Potassium (K)
- Temperature
- Humidity
- Soil pH
- Rainfall

---

## 📂 Dataset

### Features

| Feature | Description |
|---------|-------------|
| N | Nitrogen content in soil |
| P | Phosphorus content in soil |
| K | Potassium content in soil |
| Temperature | Temperature (°C) |
| Humidity | Relative Humidity (%) |
| pH | Soil pH |
| Rainfall | Rainfall (mm) |

### Target

- Crop Label

---

## 🔍 Exploratory Data Analysis

The following analyses were performed:

- Dataset overview
- Missing value analysis
- Duplicate value check
- Statistical summary
- Correlation Heatmap
- Distribution Analysis
- Boxplots
- Outlier Detection using IQR

---

## 📊 Outlier Investigation

Instead of removing statistical outliers directly, each feature was investigated using agricultural domain knowledge.

### Findings

- Rainfall outliers mainly belonged to Rice, Papaya, and Coconut.
- Nutrient outliers belonged to specific crop classes.
- pH values were within realistic agricultural ranges.
- Temperature values represented genuine climatic conditions.

Since these observations represented **real agricultural scenarios rather than data errors**, no outliers were removed.

---

## 🤖 Model Development

### Algorithm

- Decision Tree Classifier

### Why Decision Tree?

- Easy to interpret
- Handles non-linear relationships
- No feature scaling required
- Robust to genuine outliers
- Provides feature importance

---

## ⚙️ Hyperparameter Tuning

Hyperparameter tuning was performed using **GridSearchCV (5-Fold Cross Validation)**.

The following parameters were optimized:

- Criterion
- Max Depth
- Minimum Samples Split
- Minimum Samples Leaf
- Maximum Features
- Cost Complexity Pruning (`ccp_alpha`)

This helped identify the optimal Decision Tree configuration while reducing overfitting.

---

## 📈 Feature Importance

Feature importance analysis showed the following ranking:

| Rank | Feature |
|------|----------|
| 1 | Rainfall |
| 2 | Phosphorus (P) |
| 3 | Humidity |
| 4 | Potassium (K) |
| 5 | Nitrogen (N) |
| 6 | Temperature |
| 7 | pH |

Rainfall was identified as the most influential feature for crop recommendation.

---

## 📊 Model Performance

### Evaluation Metrics

- Accuracy Score
- Confusion Matrix
- Classification Report

### Final Accuracy

**97%**

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

---

## 📁 Project Structure

```
Crop-Recommendation-System/
│
├── Crop_Recommendation.ipynb
├── crop_recommendation_model.pkl
├── label_encoder.pkl
├── requirements.txt
├── README.md
└── dataset.csv
```

---

## 🚀 Future Improvements

- Compare with Random Forest and XGBoost
- Deploy using Streamlit
- Integrate real-time weather API
- Fertilizer recommendation system
- Mobile-friendly crop recommendation application

---

## 🌾 Conclusion

A Decision Tree-based crop recommendation system was successfully developed with an accuracy of **97%**. Through comprehensive exploratory data analysis and domain-driven outlier investigation, genuine agricultural observations were retained, ensuring the model learned from realistic farming conditions.

Hyperparameter tuning using **GridSearchCV** improved confidence in the selected model, while feature importance analysis revealed that **rainfall, phosphorus, and humidity** were the most influential factors in crop prediction.

This system can assist farmers in selecting crops that best match their soil nutrients and environmental conditions, helping improve crop yield, optimize the use of fertilizers and water resources, reduce the risk of unsuitable crop selection, and support sustainable agriculture through data-driven decision-making.

---

## ⭐ If you found this project helpful, consider giving it a star!
