# Public Health Analytics: Heart Disease Risk Prediction

An end-to-end Machine Learning project analyzing patient clinical indicators to predict heart disease presence. Built using Python, Pandas, Matplotlib, Seaborn, and Scikit-Learn.

## Project Overview
Heart disease is a leading cause of global mortality. The goal of this project is to build an interpretable data science pipeline that:
1. Cleans and explores patient clinical data.
2. Identifies critical physiological risk factors (e.g., maximum heart rate, chest pain types).
3. Trains a Machine Learning model to classify high-risk vs. low-risk patients.

## Tech Stack
* **Language:** Python 3.14
* **Data Wrangling:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn
* **IDE:** VS Code (Jupyter Notebook extension)

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

## Key Findings & Insights
### 1. Primary Physiological Risk Drivers
Based on the Gini Feature Importance scores from the trained `RandomForestClassifier`, the top clinical indicators driving heart disease diagnosis are:
* **Maximum Heart Rate Achieved (`thalach`):** Higher maximum heart rates during stress testing strongly correlate with healthy heart function. Patients with heart disease exhibited significantly lower average peak heart rates.
* **ST Depression (`oldpeak`):** Exercise-induced ST depression relative to rest served as a critical indicator of cardiac stress and vessel occlusion.
* **Chest Pain Type (`cp`):** Asymptomatic chest pain (`cp = 3`) and atypical angina presented higher rates of disease diagnosis compared to typical angina.

### 2. Demographic Correlations
* **Age vs. Risk:** Risk of heart disease presence increases steadily beyond age 50, with peak risk observed between ages 55 and 65.
* **Sex Distribution:** In this dataset cohort, male patients displayed a higher proportion of positive heart disease diagnoses relative to female patients.

### 3. Model Performance Summary
* **Baseline Algorithm:** Random Forest Classifier (100 estimators)
* **Accuracy Score:** ~85%
* **Mean Absolute Error (MAE):** < 0.15 (indicating strong overall classification reliability across stratified test split)


## Dataset & Citation

The dataset used in this project is the **UCI Heart Disease Dataset**, made publicly available by the UCI Machine Learning Repository.

* **Original Creators / Donors:** 
  * Hungarian Institute of Cardiology. Budapest: Andras Janosi, M.D.
  * University Hospital, Zurich, Switzerland: William Steinbrunn, M.D.
  * University Hospital, Geneva, Switzerland: Matthias Pfisterer, M.D.
  * Veterans Administration Medical Center, Long Beach and Cleveland Clinic Foundation: Robert Detrano, M.D., Ph.D.
* **License:** Public Domain / CC BY 4.0
* **Repository Link:** [UCI Machine Learning Repository - Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)

**BibTeX Citation:**
```bibtex
@misc{dataset_45_heart_disease,
  author       = {Janosi, Andras and Steinbrunn, William and Pfisterer, Matthias and Detrano, Robert},
  title        = {{Heart Disease}},
  year         = {1988},
  howpublished = {UCI Machine Learning Repository},
  note         = {{DOI}: [https://doi.org/10.24432/C52P4X](https://doi.org/10.24432/C52P4X)}
}