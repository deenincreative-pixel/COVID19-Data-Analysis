# COVID19-Data-Analysis
Interactive Power BI dashboard analyzing global COVID-19 statistics including infection rates and mortality analysis.

Tools & Technologies
#Power BI Desktop : For data visualization and dashboard reporting.
#Power Query : For data cleaning, handling mssing values, and data transformation.
#Data Analysis Expressions : Used for creating advanced measures like infectio rate.

Data Cleaning Process
Before visualization, the raw dataset underwent several cleaning steps in Power Query:
#Handling Nulls : Replaced null values in critical and recovered cases with 0 to ensure calculation accuracy.
#Data Type correction : Standardized date formats and numerical values (e.g., total cases, population).
#Filtering : Removed non-geographic entries (e.g., "Diamond Princess") to maintain data integrity for spatial analysis.

Key Insights & Features
#Infection Rate Analysis : A custom DAX measure comparing total cases against the population to identify highly impacted regions regardless of population size.
#Global KPI Overview : Real-time summary of Total Cases, Recoveries, and Deaths.
#Geographical Distribution : A map visualization showing the density of deaths globally.
#Top 10 Analysis : Bar charts highlighting the top 10 countries with the highest mortlity rates.

Sample DAX Formulas
#Infection Rate : ```dax
Infection Rate = DIVIDE(SUM('covid19_statistics'[cases.total]),SUM('covid19_statistics'[population(k)]), 0)
