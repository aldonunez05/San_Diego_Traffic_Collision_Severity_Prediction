# San Diego Traffic Collision Severity Prediction

This project uses machine learning to analyze traffic collision data from San Diego and predict the severity of crashes — including whether they result in fatalities, injuries, or no harm. It also identifies key risk factors like time of day, location (police beat), and date.

---

##  Project Overview

- **Goal**: Predict crash severity (`fatal`, `injury`, `none`) from traffic report data
- **Tech**: Python, scikit-learn, pandas, seaborn, imbalanced-learn
- **Data**: Official San Diego traffic collision dataset (2015+)

---

##  Key Features

- Cleaned and preprocessed real-world traffic data
- Balanced imbalanced classes using SMOTE
- Trained and evaluated a Random Forest classifier
- Identified most important features using feature importances and SHAP
- Achieved ~95% accuracy on balanced validation, and ~81% accuracy on real-world distribution

---

## Insights

- **Police beat**, **hour**, and **month** are the top predictors of severity
- The model performs well at identifying high-risk collisions
- Potential to integrate into a real-time crash risk dashboard

---

##  File Structure
 SD-Traffic-Collision-Analysis/
│
├── notebooks/
│   ├── 01_model_tuning.ipynb
│   ├── 02_model_comparison.ipynb
│   └── 03_model_explainability.ipynb
│
├── data/
│   └── traffic_collisions_cleaned.csv
│
├── models/
│   └── best_model.pkl
│
├── README.md
├── requirements.txt
└── .gitignore


---

##  How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/San_Diego_Traffic_Collision_Severity_Prediction.git
   cd San_Diego_Traffic_Collision_Severity_Prediction
   
2. Install dependencies:
   pip install -r requirements.txt
Launch the notebook:
   jupyter notebook notebooks/crash_analysis.ipynb
---

## Example Results
| Class   | Precision | Recall | F1-Score |
|---------|-----------|--------|----------|
| Fatal   | 1.00      | 0.73   | 0.84     |
| Injury  | 0.87      | 0.71   | 0.78     |
| None    | 0.68      | 0.99   | 0.81     |

---

## Future Work
Interactive dashboard using Streamlit

Risk heatmap by police beat and time

Real-time crash severity prediction API
