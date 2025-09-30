# Diabetes Ensemble Classification

This repository contains the implementation of **homogeneous** (Boosting, Bagging) and **heterogeneous** (Stacking, Blending) ensemble learning models for **diabetes mellitus classification**.  
The project compares model accuracy, training time, and memory usage to find the most efficient approach for diabetes risk prediction.

---

## 📖 Overview
Diabetes mellitus is one of the fastest-growing chronic diseases globally. Early detection and classification play a crucial role in effective healthcare management.  
This project applies **ensemble learning techniques** to improve prediction performance by combining multiple models, making the system more robust compared to single classifiers.

---

## 📌 Key Features
- **Data Preprocessing**
  - Duplicate removal  
  - Handling missing values  
  - Feature transformation (categorical → numeric)  
  - Data balancing using **SMOTE-Tomek**

- **Models Implemented**
  - **Homogeneous Ensembles**
    - Boosting (AdaBoost + RandomForest)
    - Bagging (RandomForest)
  - **Heterogeneous Ensembles**
    - Stacking (XGBoost, Gradient Boosting, RandomForest as base learners, RF as meta-model)
    - Blending (similar to stacking but more efficient)

- **Evaluation Metrics**
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - Resource usage (training time & RAM)

---

## 📊 Results Summary
| Method     | Accuracy | Precision | Recall | F1-Score | RAM Usage | Training Time |
|------------|----------|-----------|--------|----------|-----------|---------------|
| Boosting   | 98%      | 0.98      | 0.97   | 0.98     | 2676 MB   | 386 s         |
| Bagging    | 97%      | 0.97      | 0.97   | 0.97     | 3888 MB   | 466 s         |
| Stacking   | 98%      | 0.99      | 0.97   | 0.98     | 155 MB    | 189 s         |
| Blending   | 98%      | 0.99      | 0.97   | 0.98     | 88 MB     | 37 s          |

✅ **Blending** is the most efficient in terms of time & memory.  
✅ **Stacking** offers a strong balance between performance & efficiency.  

---
## 📂 Dataset
Dataset used: [Diabetes Prediction Dataset - Kaggle](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)  

Features:  
- Age, Gender, BMI  
- Hypertension, Heart disease  
- Smoking history  
- HbA1c level, Blood glucose level  
- Diabetes status (target)

---

## 🚀 How to Run
```bash
# clone repository
git clone https://github.com/username/diabetes-ensemble-classification.git
cd diabetes-ensemble-classification

# install dependencies
pip install -r requirements.txt

# run jupyter notebook
jupyter notebook notebooks/preprocessing.ipynb
