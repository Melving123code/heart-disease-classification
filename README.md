# Heart Disease Classification (Machine Learning Project)

## Overview
This project applies machine learning techniques to predict the presence of heart disease using clinical patient data. Multiple models were developed and compared to evaluate performance, generalization, and bias-variance behavior.

---

## Dataset
This project uses the Heart Disease dataset from the UCI Machine Learning Repository.

- 303 observations  
- 13 input features  
- Binary classification:
  - 0 = No Heart Disease  
  - 1 = Heart Disease Present  

The dataset is approximately balanced, with a slight majority of non-disease cases.

---

## Data Preprocessing

### Data Cleaning
- Missing values identified in `ca` and `thal`
- Missing values handled using **median imputation**
- Invalid values (e.g., cholesterol = 0, blood pressure = 0) corrected using median replacement

### Feature Selection
Selected clinically relevant features:
- Age (`age`)
- Cholesterol (`chol`)
- Maximum heart rate (`thalach`)

Removed low-impact features:
- `fbs`
- `restecg`

### Feature Engineering
- One-hot encoding for categorical variables
- Standardization applied for models sensitive to feature scaling

---

## Models Implemented

### 1. Logistic Regression (Baseline)
- Accuracy: ~0.88  
- ROC-AUC: ~0.95  
- Strong overall performance and generalization  

### 2. Decision Tree
- Tuned using cross-validation  
- Demonstrated **overfitting** (high training accuracy, lower validation accuracy)  

### 3. Neural Network
- Demonstrated **underfitting**  
- Poor performance across training and validation  

---

## Model Evaluation
Models were evaluated using:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
- Confusion Matrix  

---

## Results & Insights

- Logistic Regression performed best overall  
- Decision Tree showed high variance (overfitting)  
- Neural Network showed high bias (underfitting)  
- Increasing model complexity did not improve performance  

---

## Key Takeaways

- Simpler models can outperform complex models on structured datasets  
- Proper preprocessing and feature selection are critical  
- Understanding bias vs variance is essential for model improvement  

---

## Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## How to Run

```bash
git clone https://github.com/Melving123code/heart-disease-classification.git
cd heart-disease-classification
pip install -r requirements.txt
