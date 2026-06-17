# HR Analytics — Employee Attrition Prediction (Elevate Labs)

Predicting employee attrition using Python (Pandas, Seaborn, Scikit-learn) and visualizing key risk factors in an interactive Power BI dashboard.

## Overview

This project analyzes the IBM HR Analytics dataset (1,470 employees, 35 features) to identify why employees leave and predict future attrition using a Decision Tree classification model. The goal is to give HR teams a data-driven tool to flag at-risk employees and act before they resign.

## Dataset

IBM HR Analytics Employee Attrition Dataset (Kaggle) — 1,470 rows, 35 columns including Age, Department, MonthlyIncome, OverTime, JobSatisfaction, and YearsAtCompany.

## Tools Used

- **Python** — Pandas, NumPy, Matplotlib, Seaborn
- **Scikit-learn** — LabelEncoder, train_test_split, DecisionTreeClassifier, accuracy_score, confusion_matrix
- **Power BI** — Interactive 3-page dashboard
- **Google Colab** — Development environment

## Project Workflow

1. **Data Loading & Exploration** — Checked shape, nulls, duplicates, and data types
2. **EDA** — Visualized attrition by department, age, income, and tenure; built a correlation heatmap
3. **Preprocessing** — Dropped redundant columns, encoded categorical features with LabelEncoder
4. **Model Building** — Trained a Decision Tree Classifier (80/20 split), achieved ~85% accuracy
5. **Model Evaluation** — Confusion matrix, classification report, and feature importance ranking
6. **Power BI Dashboard** — 3 pages built on the cleaned, exported dataset

## Key Insights

- Overall attrition rate: **16.1%** (237 of 1,470 employees)
- Top attrition drivers (feature importance): **Monthly Income**, **OverTime**, **Age**, **Job Satisfaction**, **Years at Company**
- Employees working **OverTime** show a much higher relative attrition rate (416 left vs 1,054 stayed without overtime)
- **Research & Development** has the highest attrition count (961), followed by **Sales** (446) and **Human Resources** (63)
- By marital status, **Married** employees recorded the highest attrition count (673), ahead of **Single** (470) and **Divorced** (327)
- Attrition spikes sharply around the **5-year** and **9-year** tenure marks

## Dashboard Pages

| Page | Contents |
|------|----------|
| Executive Overview | KPI cards, attrition donut chart, department & job role breakdown |
| Deep Dive Analysis | Income vs attrition, overtime vs attrition, marital status, tenure |
| Prevention Insights | Top risk factors, high-risk employee table, job satisfaction analysis |

## Repository Structure

```
hr-attrition-analysis/
│
├── hr_attrition.ipynb              # Full Python notebook (EDA + ML model)
├── hr_attrition_cleaned.csv        # Cleaned dataset used for Power BI
├── HR_Attrition_Dashboard.pbix     # Power BI dashboard file
├── HR_Attrition_Project_Report.pdf # 2-page project report
└── README.md
```

## Model Performance

- **Algorithm:** Decision Tree Classifier (max_depth=5)
- **Accuracy:** ~85%
- **Evaluation:** Confusion matrix, precision/recall/F1-score, feature importance

## Recommendations

1. Review compensation for lower income bands
2. Monitor and limit excessive overtime, especially in Research & Development and Sales
3. Implement retention check-ins around the 5-year and 9-year tenure milestones
4. Run regular job satisfaction surveys, with focused attention on married employees

## Author

**Mohammad Sadique**
LinkedIn: https://www.linkedin.com/in/mohammad-sadique-1028ba2a1
Portfolio: https://sadique-osman.github.io/portfolio
GitHub: https://github.com/Sadique-Osman
