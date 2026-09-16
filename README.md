# Public Health Analytics: Heart Disease Risk Prediction

An end-to-end Machine Learning project analyzing patient clinical indicators to predict the presence of heart disease. Built using Python, Pandas, Matplotlib, Seaborn, and Scikit-Learn.

---

## Project Overview
Heart disease is a leading cause of global mortality. The goal of this project is to build an interpretable data science pipeline that:
1. Cleans and explores patient clinical data.
2. Identifies critical physiological risk factors (e.g., maximum heart rate, chest pain types).
3. Trains a Machine Learning model to classify high-risk vs. low-risk patients.

---

## Tech Stack
* **Language:** Python 3.14
* **Data Wrangling:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest Classifier, StandardScaler)
* **IDE & Environment:** VS Code (Jupyter Notebook extension)
* **Version Control:** Git, GitHub

---

## Key Findings & Interpretation

### 1. Data Quality & Leakage Prevention
* **Deduplication Impact:** The initial dataset contained 1,025 rows, but exact duplicate checking revealed **723 redundant records**.
* **Leakage Avoidance:** Removing these duplicates reduced the dataset to **302 unique patient profiles**, successfully preventing data leakage between the training and test sets and ensuring realistic model evaluation.
* **Outlier Profile:** Outlier screening showed **1 patient** with extreme cholesterol levels (>500 mg/dl) and **0 patients** with extreme resting blood pressure (>200 mm Hg).

### 2. Model Performance
* **Overall Accuracy:** The Random Forest Classifier achieved an **80.33% accuracy score** on the 20% stratified test set (61 patient samples).
* **Low Residual Error:** The model achieved a **Mean Absolute Error (MAE) of 0.1967**, demonstrating strong calibration for binary risk classification.
* **Balanced Metrics:** 
  * **No Disease (Class 0):** Precision = `0.77`, Recall = `0.82`, F1-Score = `0.79`
  * **Heart Disease (Class 1):** Precision = `0.84`, Recall = `0.79`, F1-Score = `0.81`
* **Clinical Safety:** A high precision score (`84%`) for positive disease cases minimizes false alarms, while an `81%` F1-score balances safety and diagnostic reliability.

### 3. Key Physiological Risk Drivers
* **Exercise Stress Response (`thalach`):** Maximum heart rate achieved during exercise emerged as a primary predictive feature, showing a strong negative correlation with heart disease risk.
* **ST Depression (`oldpeak`):** Electrocardiogram changes during exercise relative to rest provided strong discriminatory power for underlying cardiac stress.
* **Symptom Mapping (`cp`):** Specific chest pain configurations serve as heavy indicators for model classification pathways.

---

## Project Structure

```text
heart-disease-prediction/
│
├── data/
│   └── heart.csv                   # Raw clinical dataset
├── notebooks/
│   └── heart_disease_analysis.ipynb # Complete EDA & ML pipeline
├── .gitignore                      # Git exclusion rules
├── README.md                       # Project documentation
└── requirements.txt                # Python environment dependencies

@misc{dataset_45_heart_disease,
  author       = {Janosi, Andras and Steinbrunn, William and Pfisterer, Matthias and Detrano, Robert},
  title        = {{Heart Disease}},
  year         = {1988},
  howpublished = {UCI Machine Learning Repository},
  note         = {{DOI}: [https://doi.org/10.24432/C52P4X](https://doi.org/10.24432/C52P4X)}
}