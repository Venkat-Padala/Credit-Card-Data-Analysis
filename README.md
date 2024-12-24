# Credit Card Data Analysis and Visualization Project

### Project Overview

This project involves analyzing and visualizing credit card data to gain insights into various factors influencing credit behavior and status. The analysis was performed using Python (NumPy, Pandas) for data cleaning and preprocessing, and Power BI for data visualization.

### Data Overview
The dataset includes various credit card usage and demographic information. Key attributes in the dataset are:

- Credit status (NPA Status)

- Revolving utilization of unsecured lines

- Age, Gender, Region

- Monthly Income, Housing Status (Rented/Owned)

- Occupation, Education

- Number of times payments were past due (30-59, 60-89, 90 days)

- Debt Ratio

- Number of open credit lines and loans, real estate loans

- Number of Dependents

- Good/Bad credit status

### Data Cleaning and Preprocessing
- Removed duplicate columns to ensure data consistency.

- Handled missing values using the mean for numerical columns:

df['NumberOfDependents'] = df['NumberOfDependents'].fillna(df['NumberOfDependents'].mean())
df['MonthlyIncome'] = df['MonthlyIncome'].fillna(df['MonthlyIncome'].mean())

* Identified and treated outliers using the Interquartile Range (IQR) method:


Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3 - Q1
outliers = ((df < (Q1 - 1.5 * IQR)) | (df > (Q3 + 1.5 * IQR)))
### Data Analysis and Visualization
- Visualization Tools Used: Power BI

#### Key Visualizations:

- Pie charts, bar charts, line graphs, and scatter plots to represent various data distributions and relationships.

- Geographical distribution of open credit lines and loans.

- Analysis of income distribution by gender, age distribution, debt ratio, and late payment patterns.


![task_01 Dashboard_page-0001](https://github.com/user-attachments/assets/4c0f2ae5-b777-4a1d-962c-211a50acf28d)


### Insights and Findings
#### Gender and Monthly Income:
 Higher median income for males compared to females, indicating potential gender disparity.

#### Housing Status and Credit Behavior:
 Homeowners have higher revolving utilization of unsecured lines.

#### Debt Ratio and Credit Risk:
 Higher debt ratios are associated with "Bad" credit status.

#### Age Distribution:
 Majority of users are within the 30-50 age range.

#### Late Payment Patterns:
 Frequent late payments significantly impact credit status.

### Conclusion
The analysis highlighted key factors influencing credit behavior and status, including income disparity, housing status, debt ratio, and late payment patterns. Recommendations include implementing financial literacy programs, providing targeted financial support, and considering policy interventions to address income and credit disparities.
