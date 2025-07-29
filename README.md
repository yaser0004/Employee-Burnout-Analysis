
# Employee Burnout Analysis

This project, falling under the domain of **Data Science**, performs a comprehensive analysis of an employee dataset to explore factors contributing to burnout. The workflow involves data loading, cleaning, statistical inspection, visualization, and preprocessing—covering areas such as data analysis, exploratory data analysis (EDA), and feature engineering—to understand patterns and prepare the data for potential future machine learning applications.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Key Visualizations](#key-visualizations)
- [Technologies Used](#technologies-used)
- [Future Work](#future-work)
- [Final Conclusion](#final-conclusion)

---

## Overview

The goal of this project is to analyze an employee dataset with a focus on understanding burnout levels. The analysis includes:
- Exploratory data inspection
- Null value detection and imputation
- Visualizations of categorical and numerical variables
- Encoding and normalization for machine learning readiness

No predictive model is built in this notebook, but the dataset is preprocessed thoroughly for future use in classification or regression tasks.

---

## Dataset

- Source: [Google Sheets - Employee Burnout Dataset](https://docs.google.com/spreadsheets/d/1zz4Y_pxx0bJgb71dTTrVH8YVezopb8Js/edit?usp=drive_link&ouid=117555289042853628777&rtpof=true&sd=true)
- Key columns include:
  - `Employee ID`
  - `Date of Joining`
  - `Gender`
  - `Company Type`
  - `WFH Setup Available`
  - `Designation`
  - `Resource Allocation`
  - `Mental Fatigue Score`
  - `Burn Rate` *(target variable)*

---

## Project Structure

### 1. Data Loading
- The dataset is loaded using `pandas.read_csv()`.
- Initial structural checks (`head()`, `info()`, `describe()`).

### 2. Exploratory Data Analysis
- Value counts and null value inspection.
- Grouping and basic statistical analysis by categories (e.g., by `gender`, `company_type`, etc.).

### 3. Data Visualization
- Count plots for gender, company type, remote work availability, and designation.
- Distribution plots for mental fatigue and resource allocation.
- Heatmap for correlation matrix.
- Boxplots for examining burnout distribution across categories.

### 4. Data Preprocessing
- Dropping uninformative columns like `Employee ID` and `Date of Joining`.
- Handling missing values:
  - `Mental Fatigue Score`: filled with median.
  - `Burn Rate`: filled with mean.
- Encoding categorical variables using `LabelEncoder`.
- Normalization using `MinMaxScaler`.

---

## Key Visualizations

- **Categorical Count Plots**: Understand distribution of employees across categories.
- **Burn Rate vs Gender/Company**: Boxplots to show how burnout varies across groups.
- **Heatmap**: Shows correlation between numerical features.
- **Distribution Plots**: For resource allocation and fatigue scores.

---

## Technologies Used

- **Python 3**
- **Pandas**: data manipulation
- **NumPy**: numerical operations
- **Seaborn** and **Matplotlib**: visualization
- **Scikit-learn**: preprocessing

---

## Future Work

- Implement predictive models (classification or regression) for burnout.
- Perform hyperparameter tuning and model evaluation.
- Integrate dashboards using Streamlit or Plotly Dash for interactive exploration.
- Apply feature engineering and dimensionality reduction if needed.

---

## Final Conclusion

This project prepared and explored an employee dataset with the objective of understanding key contributors to employee burnout. After data cleaning, visualization, and transformation, the following key insights were identified:

### 🔍 Key Findings:
- **Gender Impact**: Slight differences in burnout were observed between male and female employees, though not extreme.
- **Company Type**: Employees working in **private sector companies** generally showed **higher burnout levels** than those in public sector companies.
- **Remote Work**: Employees **without a work-from-home setup** exhibited **slightly higher burnout**, indicating the potential benefit of flexible work arrangements.
- **Designation Level**: Burnout tends to **increase with seniority**, suggesting higher responsibility may be a stressor.
- **Mental Fatigue**: Strongly correlated with burnout—higher fatigue scores directly align with increased burnout.
- **Resource Allocation**: Both **under-allocation** and **over-allocation** of resources are associated with higher burnout, highlighting the need for balanced workloads.

### ✅ Final Result:
- The dataset was thoroughly analyzed and preprocessed (missing values handled, features encoded and scaled).
- The cleaned and structured dataset is now **ready for training machine learning models** in future work.
- Clear **risk indicators** (fatigue, workload, role, company type) were identified that can help organizations act proactively to reduce burnout.

This analysis lays the groundwork for building robust predictive systems to identify and reduce employee burnout, ultimately helping companies protect mental health and productivity.
