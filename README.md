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
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
│
├── 📂 notebooks/
│   └── HR_Attrition_Analysis.ipynb
│
├── 📂 images/
│   ├── attrition_distribution.png
│   ├── correlation_heatmap.│   ├── feature_importance.png
│   └── confusion_matrix.png
│
├── 📄 README.md
├── 📄 requirements.txt
└── 📄 LICENSE

## 🔄 Analysis Workflow

┌──────────────────┐
│ 1. Data Loading   │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 2. Data Cleaning  │
│ • Missing values  │
│ • Duplicates      │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 3. Exploratory    │
│    Data Analysis  │
│ • Statistics      │
│ • Visualizations  │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 4. Feature        │
│    Engineering    │
│ • Encoding        │
│ • Scaling         │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 5. Model Building │
│ • Train/Test      │
│ • Logistic Reg.   │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 6. Evaluation     │
│ • Accuracy        │
│ • Confusion Mat.  │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ 7. Insights &     │
│    Recommendations│
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

