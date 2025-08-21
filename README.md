# HR Attrition Exploratory Data Analysis (EDA)

##  Project Overview
This project explores employee attrition patterns using the **HR Employee Attrition** dataset. The goal is to uncover insights related to turnover trends and identify actionable business strategies for improving employee retention.

##  Table of Contents
1. [Dataset Description](#dataset-description)  
2. [Objective](#objective)  
3. [Data Cleaning](#data-cleaning)  
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
   - Univariate Analysis  
   - Bivariate Analysis  
   - Correlation Analysis  
5. [Key Findings](#key-findings)  
6. [Business Insights & Recommendations](#business-insights--recommendations)  
---

##  Dataset Description
- **Source**: Kaggle — HR Employee Attrition dataset  
- **Rows**: 1,470  
- **Columns**: 35, including features like `Age`, `BusinessTravel`, `Department`, `MonthlyIncome`, `OverTime`, `YearsAtCompany`, and the target variable `Attrition`.

---

##  Objective
- Analyze factors influencing employee attrition  
- Identify trends and patterns related to turnover  
- Derive actionable recommendations to improve employee retention

---

Data Cleaning
Dropped columns with no analytical value:
```python
columns_to_drop = ["EmployeeCount", "StandardHours", "Over18", "EmployeeNumber"]
df.drop(columns=columns_to_drop, inplace=True)

---

Exploratory Data Analysis (EDA)

1. Univariate Analysis

Attrition: Significant class imbalance—~240 employees left vs. ~1,220 who stayed

Age: Bell-shaped distribution, most employees aged between 30–35

Monthly Income: Right-skewed; most employees earn ₹2,500–₹3,000/month, few earn above ₹15,000

2. Bivariate Analysis

Attrition by Job Role: Highest turnover in Sales Executive, Research Scientist, and Laboratory Technician roles

OverTime vs. Attrition: Employees working overtime leave at much higher rates

Age vs. Monthly Income (with Attrition indicator):

Younger, lower-income employees are more likely to leave

Older, higher-income employees are more stable

Years at Company vs. Attrition:

Higher attrition among employees with ≤5 years of tenure

Very low attrition for those with 15+ years of service

3. Correlation Analysis

Heatmap of numerical features reveals relationships among tenure, income, satisfaction, and performance metrics. (See notebook for full visualization.)

Key Findings

Attrition Clusters: Sales Executives and Research Scientists show notably high attrition.

OverTime Risk: Overtime usage significantly correlates with attrition, suggesting burnout.

Age & Income Dynamics: Younger employees with low pay are most likely to quit.

Tenure Effect: Early years (1–5) are critical — most attrition occurs within this period.

Business Insights & Recommendations

Insight	Action
 - High attrition in certain job roles	Investigate workload, job satisfaction, and workload in Sales, Research, and Technical teams

 - Overtime linked to attrition	Reevaluate and optimize overtime policies; offer wellness programs

 - Younger, low-paid employees most at risk	Develop career development paths and compensation incentives

 - Early-stage attrition	Implement onboarding and mentorship programs to boost early-career engagement
