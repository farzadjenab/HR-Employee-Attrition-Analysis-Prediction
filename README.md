# 🏢 HR Employee Attrition Analysis & Prediction

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-0.24+-orange.svg)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Analysis Workflow](#-analysis-workflow)
- [Key Findings](#-key-findings)
- [Model Performance](#-model-performance)
- [Visualizations](#-visualizations)
- [Technologies Used](#-technologies-used)
- [Future Improvements](#-future-improvements)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

> **Employee attrition** is a critical challenge for organizations, leading to increased costs in recruitment, training, and lost productivity.

This project performs a comprehensive **Exploratory Data Analysis (EDA)** and builds a **predictive model** to identify employees who are likely to leave the company. By understanding the key factors driving attrition, HR departments can implement targeted retention strategies.

### 🎯 Project Objectives

| # | Objective |
|---|-----------|
| 1 | Explore and understand the HR dataset |
| 2 | Identify key factors contributing to employee attrition |
| 3 | Visualize patterns and relationships in the data |
| 4 | Build a predictive model using Logistic Regression |
| 5 | Provide actionable recommendations for HR |

---

## 📊 Dataset

### Source
- **Name:** IBM HR Analytics Employee Attrition & Performance
- **Records:** 1,470 employees
- **Features:** 35 attributes

### Key Features

| Category | Features |
|----------|----------|
| **Demographics** | `Age`, `Gender`, `MaritalStatus`, `DistanceFromHome` |
| **Job-Related** | `Department`, `JobRole`, `JobLevel`, `YearsAtCompany` |
| **Compensation** | `MonthlyIncome`, `PercentSalaryHike`, `StockOptionLevel` |
| **Satisfaction** | `JobSatisfaction`, `EnvironmentSatisfaction`, `WorkLifeBalance` |
| **Performance** | `PerformanceRating`, `TrainingTimesLastYear` |
| **Target** | `Attrition` (Yes/No) |

### Target Variable Distribution
┌─────────────┬───────┬────────────┐

│ Attrition │ Count │ Percentage │

├─────────────┼───────┼────────────┤

│ No │ 1,233 │ 83.9% │

│ Yes │ 237 │ 16.1% │

└─────────────┴───────┴────────────┘
## 📁 Project Structure
hr-attrition-analysis/
│
├── 📂 data/
│ └── WA_Fn-UseC_-HR-Employee-Attrition.csv
│
├── 📂 notebooks/
│ └── HR_Attrition_Analysis.ipynb
│
├── 📂 images/
│ ├── attrition_distribution.png
│ ├── correlation_heatmap.png
│ ├── feature_importance.png
│ └── confusion_matrix.png
│
├── 📄 README.md
├── 📄 requirements.txt
└── 📄 LICENSE


## 🚀 Installation
### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
### Step-by-Step Setup
1. Clone the repository


bash
   git clone https://github.com/farzadjenab/HR-Employee-Attrition-Analysis-Prediction?tab=readme-ov-file#-project-structure

2. Create a virtual environment (optional but recommended)


bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install dependencies

bash
   pip install -r requirements.txt
4. Launch Jupyter Notebook

bash
   jupyter notebook
### Requirements


pandas>=1.3.0

numpy>=1.21.0

matplotlib>=3.4.0

seaborn>=0.11.0

scikit-learn>=0.24.0

jupyter>=1.0.0
## 🔄 Analysis Workflow

┌──────────────────┐

│ 1. Data Loading │

└────────┬─────────┘

▼

┌──────────────────┐

│ 2. Data Cleaning │

│ • Missing values│

│ • Duplicates │

└────────┬─────────┘

▼

┌──────────────────┐

│ 3. Exploratory │

│ Data Analysis │

│ • Statistics │

│ • Visualizations│

└────────┬─────────┘

▼

┌──────────────────┐

│ 4. Feature │

│ Engineering │

│ • Encoding │

│ • Scaling │

└────────┬─────────┘

▼

┌──────────────────┐

│ 5. Model Building│

│ • Train/Test │

│ • Logistic Reg. │

└────────┬─────────┘

▼

┌──────────────────┐

│ 6. Evaluation │

│ • Accuracy │

│ • Confusion Mat.│

└────────┬─────────┘

▼

┌──────────────────┐

│ 7. Insights & │

│ Recommendations │

└──────────────────┘

## Key Findings
### Factors Increasing Attrition

| Factor           | Impact     | Details                                              |
|------------------|------------|------------------------------------------------------|
| ⏱️ Overtime       | Very High  | Employees with overtime have ~30% attrition rate     |
| 💰 Low Income     | High       | Lower income correlates with higher attrition        |
| 💍 Single Status  | Medium     | Single employees leave more frequently               |
| 🧑‍💼 New Employees | Medium     | Less tenure = higher attrition risk                  |
| 🙂 Low Satisfaction| Medium     | Both job and environment satisfaction matter         |

### Factors Decreasing Attrition
| Factor             | Impact  | Details                                             |
|--------------------|---------|-----------------------------------------------------|
| 💵 Higher Income    | High    | Better compensation retains employees               |
| ⚖️ Work‑Life Balance | High    | Score of 3–4 significantly reduces attrition        |
| 📅 Tenure          | Medium  | More years at company = less likely to leave        |
| 🎖️ Promotions      | Medium  | Recent promotions improve retention                 |

### Attrition by Department

- Sales: 21%
- Human Resources: 19%
- Research & Development: 14%

### 3 Job Roles with Highest Attrition

1. 🥇 Sales Representative – 40%
2. 🥈 Laboratory Technician – 24%
3. 🥉 Human Resources – 23%

## 🤖 Model Performance
### Algorithm: Logistic Regression

| Metric          | Score  |
|-----------------|--------|
| Accuracy        | 87.4%  |
| Precision (Yes) | 62%    |
| Recall (Yes)    | 28%    |
| F1‑Score (Yes)  | 39%    |

## Confusion Matrix
#### Predicted

┌─────┬─────┐

│ No │ Yes │

┌──────┼─────┼─────┤

Actual │ No │ 243 │ 10 │

├──────┼─────┼─────┤

│ Yes │ 27 │ 14 │

└──────┴─────┴─────┘

### Feature Importance
OverTime ████████████████████ +0.82

NumCompaniesWorked ██████████░░░░░░░░░░ +0.41

DistanceFromHome ████████░░░░░░░░░░░░ +0.32

───────────────────────────────────────────────

YearsAtCompany ████████░░░░░░░░░░░░ -0.35

TotalWorkingYears ██████████░░░░░░░░░░ -0.44

MonthlyIncome ████████████░░░░░░░░ -0.51

🔴 Positive coefficients = Increase attrition risk

🟢 Negative coefficients = Decrease attrition risk

## 📊 Visualizations
### Attrition Distribution
Pie chart showing the imbalanced nature of the dataset

### Correlation Heatmap
Identifying relationships between numerical features

### Attrition by Various Factors
- Age distribution by attrition status
- Monthly income comparison
- Overtime impact analysis
- Department-wise breakdown
### Model Results
- Confusion matrix heatmap
- Feature importance bar chart

## 🛠️ Technologies Used

| Language     | Data Analysis | Visualization | Machine Learning      |
|--------------|---------------|---------------|------------------------|
| Python 3.8+  | Pandas        | Matplotlib    | Scikit‑Learn          |
| Jupyter      | NumPy         | Seaborn       | Logistic Regression   |

## Future Improvements

- [ ] Handle Class Imbalance — Implement SMOTE or class weights  
- [ ] Try More Algorithms — Random Forest, XGBoost, SVM  
- [ ] Hyperparameter Tuning — GridSearchCV optimization  
- [ ] Cross‑Validation — K‑Fold for robust evaluation  
- [ ] Feature Engineering — Create new meaningful features  
- [ ] Build Dashboard — Interactive Streamlit/Dash app  
- [ ] API Deployment — Flask/FastAPI for predictions

## 🤝 Contributing

Contributions are welcome! Here’s how you can help:

1. Fork the repository
2. Create a new branch


bash
   git checkout -b feature/YourFeature
3. Commit your changes


bash
   git commit -m "Add YourFeature"
4. Push to the branch


bash
   git push origin feature/YourFeature

5. Open a Pull Request


## 📄 License
This project is licensed under the MIT License.

## 👤 Author
Farzad Jenab
📧 Email: jenabfarzad@yahoo.com
💼 LinkedIn: farzadjenab
🐱 GitHub: @farzadjenab
## ⭐ Show Your Support
If you found this project helpful, please give it a ⭐ on GitHub!

<div align=“center”>

Made with ❤️ and Python

Happy Analyzing! 📊

</div>


