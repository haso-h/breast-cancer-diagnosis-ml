# Breast Cancer Diagnosis – Machine Learning Project

## Overview
This project demonstrates the complete process of building a **Machine Learning solution** for breast cancer diagnosis based on 30 medical features derived from cell nuclei measurements.  
The goal is to classify tumor samples into diagnostic categories using various supervised learning algorithms.

---

## Dataset
- **Number of samples:** 285 records (training set)  
- **Number of features:** 30 numerical features plus ID and class label.  
- **Target variable:** `class` – diagnostic outcome of the tumor sample.  
- Additional test set provided for final predictions.  
- Dataset is not included in this repository due to licensing restrictions. The notebook can be executed locally after adding the data to the `/data` directory.

---

## Data Preprocessing
- Replaced placeholder values (`"?"`, `"NA"`, `"null"`, `"None"`) with `NaN`.  
- Converted all applicable columns to numeric types.  
- Checked for missing values and empty strings.  
- Removed non-informative columns such as `ID`.  
- Standardized all features using `StandardScaler`.  
- Split the data into **train (80%) and test (20%) sets** with stratification to preserve class balance.

---

## Machine Learning Models
The project implements and compares multiple supervised classification algorithms:

1. Logistic Regression  
2. Random Forest Classifier  
3. XGBoost Classifier  

For all models:
- **GridSearchCV** with 5-fold cross-validation was used for hyperparameter tuning.  
- Evaluation metrics included Accuracy, Precision (macro), Recall (macro), F1-score (macro), and Confusion Matrix.  
- Final predictions for the test dataset were exported to a `.csv` submission file.

