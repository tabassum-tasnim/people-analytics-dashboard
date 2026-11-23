# 👥 People Analytics Dashboard

## Overview
Interactive analytics dashboard providing insights into employee attrition, engagement, and performance drivers.

## Business Problem
Employee turnover costs companies 50-200% of annual salary. This dashboard helps HR teams:
- Identify at-risk employees before they leave
- Understand key drivers of attrition
- Make data-driven retention decisions


## Key Findings

- **Attrition patterns:** Attrition varied across employee characteristics, including age, monthly income and organizational tenure.
- **Early-tenure employees:** Employees with shorter organizational tenure showed elevated attrition rates in the exploratory analysis.
- **Job satisfaction:** Job satisfaction differed significantly between employees who stayed and those who left in the analyzed dataset.
- **Predictive modeling:** Monthly income had the highest reported Random Forest feature importance. However, feature importance does not establish a causal relationship with attrition.

These findings describe associations within the IBM HR Analytics dataset. They should not be interpreted as causal explanations or generalized to other organizations without further validation.

## Features
- Interactive workforce overview
- Attrition analysis by department, role, and tenure
- Performance & engagement insights with statistical validation
- Attrition risk analysis using transparent rule-based segments, alongside saved machine-learning evaluation metrics and feature-importance summaries


## Tech Stack
- **Data Processing**: Python, Pandas, NumPy
- **Modeling**: Scikit-learn, Random Forest
- **Statistical Analysis**: SciPy
- **Visualization**: Plotly, Matplotlib, Seaborn
- **Dashboard**: Streamlit
- **Deployment**: Streamlit Cloud (coming soon)


## Model Performance

A Random Forest classifier was evaluated on a stratified 20% test split of the IBM HR Analytics dataset.

| Metric | Score |
|---|---:|
| Accuracy | 75% |
| ROC-AUC | 0.670 |
| Precision (employees who left) | 28% |
| Recall (employees who left) | 36% |

Monthly income had the highest reported feature importance (25.3%).

**Limitations:** The model demonstrated limited ability to identify employees who left, missing approximately 64% of positive cases in the test set. These results come from a historical sample rather than external validation. The dashboard displays saved model metrics and rule-based risk segments; it does not currently generate individual predictions using the trained model.

The analysis is intended as a demonstration of exploratory people analytics, not as a validated system for making employment decisions.


## Installation

```bash
# Clone the repository
git clone https://github.com/tabassum-tasnim/people-analytics-dashboard.git

# Navigate to project directory
cd people-analytics-dashboard

# Install dependencies
pip install -r requirements.txt

# Run the dashboard
streamlit run app/streamlit_app.py
```

## Project Structure
```
people-analytics-dashboard/
├── data/
│   ├── WA_Fn-UseC_-HR-Employee-Attrition.csv
│   └── cleaned_data.csv
├── notebooks/
│   └── Data Analysis & Insights.ipynb
├── models/
│   └── attrition_model.pkl
├── app/
│   └── streamlit_app.py
├── requirements.txt
└── README.md
```

## Future Enhancements
- Real-time data integration
- Sentiment analysis from employee surveys
- Predictive prescriptive recommendations
- A/B testing for retention interventions

## Author
**Tasnim Tabassum**  
Data Scientist | Machine Learning Engineer  
[LinkedIn](https://www.linkedin.com/in/towmony) | [Portfolio](https://tabassum-tasnim.github.io/)


## Dataset
IBM HR Analytics Employee Attrition Dataset (Kaggle)
