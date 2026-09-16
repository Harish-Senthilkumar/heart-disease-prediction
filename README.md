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