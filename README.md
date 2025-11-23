# Heart Disease Prediction using Machine Learning

This project builds a machine learning system to predict whether a patient has **heart disease** using clinical and physiological attributes. The project can be categorized under a binary classification task. The goal is to explore the dataset, preprocess the features, build predictive models, and compare their performance.

---

## Problem Overview

The dataset contains key medical attributes such as age, chest pain type, resting blood pressure, cholesterol level, ECG results, heart rate, and more.

The target variable:

| Class | Meaning |
|-------|----------|
| **0** | No Heart Disease |
| **1** | Heart Disease |

### **Dataset Features (from problem statement)**

| Feature | Description | Type |
|---------|-------------|------|
| **age** | Age in years | Numeric |
| **sex** | 0 = Female, 1 = Male | Binary |
| **chest pain type** | 1: Typical Angina<br>2: Atypical Angina<br>3: Non-anginal Pain<br>4: Asymptomatic | Nominal |
| **resting bp** | Resting blood pressure (mm Hg) | Numeric |
| **cholesterol** | Serum cholesterol (mg/dl) | Numeric |
| **fasting blood sugar** | 0: <120 mg/dl, 1: >120 mg/dl | Binary |
| **resting ecg** | 0: Normal<br>1: ST-T abnormality<br>2: Left ventricular hypertrophy | Nominal |
| **max heart rate** | Maximum heart rate (71–202) | Numeric |
| **exercise angina** | 0 = No, 1 = Yes | Binary |
| **oldpeak** | ST depression | Numeric |
| **ST slope** | 1: Upward<br>2: Flat<br>3: Downward | Nominal |
| **target** | 0 = Normal, 1 = Heart Disease | Binary |

## 🧠 Approach & Methodology

### **1. Exploratory Data Analysis**
- Distribution of key medical indicators  
- Correlation heatmaps  
- Outlier inspection  
- Class imbalance check  

### **2. Preprocessing**
- Handled categorical features using encoding  
- Scaled numerical values using StandardScaler  
- Applied feature selection (Variance Threshold, SelectKBest, RFE)  
- Split dataset into train/test sets

### **3. Hyperparameter Tuning**
- Used **RandomizedSearchCV** to tune LightGBM  
- Tuned parameters like:
  - `num_leaves`, `max_depth`, `learning_rate`
  - `n_estimators`, `min_child_samples`
  - `subsample`, `colsample_bytree`

### **3. Models Trained**
A LightGBM model was trained for this classification task.

### **4. Evaluation Metrics**

### Classification Report (Proper Table)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| **0** | 0.95 | 0.93 | 0.94 | 107 |
| **1** | 0.94 | 0.96 | 0.95 | 131 |
| **Accuracy** |  |  | **0.95** | 238 |
| **Macro Avg** | 0.95 | 0.94 | 0.94 | 238 |
| **Weighted Avg** | 0.95 | 0.95 | 0.95 | 238 |

Test accuracy: 94.5%


