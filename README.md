# Mutual-Fund-Performance-Analysis-Dashboard
Mutual Fund Performance Analysis using Python and Power BI
Course: Data Analytics
Project: Mutual Fund Performance Analysis Dashboard
Tools Used: Python, Excel, Power BI
1. Business Problem
Mutual fund investors often face difficulties in comparing thousands of available funds
based on multiple financial metrics such as returns, risk, expense ratio, and fund size.
Making investment decisions without proper analysis can lead to poor portfolio
performance.
The objective of this project is to build an interactive analytical dashboard that helps
investors compare mutual funds, identify top-performing funds, evaluate risk-adjusted
returns, and make informed investment decisions.
2. Project Objectives
The primary objectives of this project are:
• Analyze mutual fund performance across different categories.
• Compare funds using multiple return periods (1 Year, 3 Years, and 5 Years).
• Evaluate investment risk using Beta and Sharpe Ratio.
• Identify the best-performing mutual funds.
• Study the relationship between risk and returns.
• Provide interactive dashboards for business decision-making.
3. Dataset Description
The dataset contains detailed information about various Indian mutual funds.
Important Columns
Column Description
Scheme Name Name of Mutual Fund
AMC Name Asset Management Company
Column Description
Category Fund Category
Returns 1Y One-Year Return
Returns 3Y Three-Year Return
Returns 5Y Five-Year Return
Expense Ratio Annual Fund Expense
Sharpe Ratio Risk-adjusted Return Measure
Beta Market Risk Indicator
Fund Size Assets Under Management (₹ Cr)
Risk Level Investment Risk Category
4. Methodology
The project was completed in the following stages:
Step 1: Data Collection
Collected the mutual fund dataset containing performance metrics and fund details.
Step 2: Data Cleaning
Performed data cleaning using Python:
• Removed duplicate records.
• Handled missing values.
• Corrected inconsistent category names.
• Converted data types.
• Removed unwanted columns.
Step 3: Exploratory Data Analysis (EDA)
EDA was performed using:
• Pandas
• Matplotlib
• Seaborn
The analysis focused on:
• Return distributions
• Category comparisons
• Expense ratio analysis
• Risk analysis
• Fund size distribution
Step 4: Feature Engineering
Created additional fields including:
• Composite Score
• Rank
• Selected Return (Dynamic Measure)
• Average Return
• Average Sharpe Ratio
Step 5: Dashboard Development
Developed an interactive Power BI dashboard using:
• KPI Cards
• Bar Charts
• Scatter Plot
• Pie Chart
• Summary Table
• Dynamic Slicers
• Tooltips
• Drill-through
• Cross Filtering
5. Tools and Technologies
Tool Purpose
Python Data Cleaning & Analysis
Pandas Data Manipulation
NumPy Numerical Operations
Matplotlib Data Visualization
Seaborn Statistical Visualization
Excel Data Validation
Power BI Dashboard Development
DAX Measures and KPIs
6. Dashboard Features
The dashboard contains the following visualizations.
KPI Cards
• Average Return
• Average Expense Ratio
• Average Sharpe Ratio
• Total Fund Size
Top 30 Mutual Funds
Displays the top 30 mutual funds based on the selected return period.
Features:
• Dynamic ranking
• Tooltips
• Drill-down
• Drill-through
Average Returns by Category
Compares average returns across categories.
Supports:
• Category hierarchy
• Dynamic return period
Risk (Beta) vs Return Scatter Plot
Analyzes the relationship between investment risk and returns.
Bubble Size:
• Fund Size
Category Distribution
Pie chart showing the number of funds in each category.
Summary Table
Displays:
• Scheme Name
• AMC
• Category
• Return
• Expense Ratio
• Sharpe Ratio
• Beta
• Rank
Slicers
Interactive filters include:
• Category
• Return Period
• AMC
• Risk Level
7. Business Insights
Insight 1
Equity mutual funds generated the highest average returns compared to other
categories.
Insight 2
Several top-performing funds achieved high returns while maintaining moderate
expense ratios.
Insight 3
Funds with higher Sharpe Ratios generally delivered better risk-adjusted performance.
Insight 4
The scatter plot indicates that higher risk does not always guarantee higher returns.
Insight 5
Large fund size does not necessarily imply superior returns, emphasizing the need for
comprehensive performance evaluation.
Insight 6
Long-term investment performance (5-Year Return) provides a better indication of
consistent fund performance than short-term returns.
Insight 7
Interactive filtering enables investors to compare funds by category, AMC, and risk level,
improving investment analysis.
8. Key Findings
• Equity funds outperform most categories in long-term returns.
• Low expense ratios alone do not guarantee higher returns.
• Sharpe Ratio is an effective metric for evaluating risk-adjusted performance.
• Dynamic return-period analysis helps compare short-term and long-term
investment strategies.
• Investors should evaluate multiple financial metrics instead of relying on returns
alone.
9. Recommendations
Based on the analysis:
• Investors should prioritize funds with high Sharpe Ratios and consistent long-
term returns.
• Expense Ratio should be considered along with return performance.
• Diversifying investments across categories can reduce portfolio risk.
• Long-term returns provide a more reliable measure than short-term
performance.
• Investors should analyze both risk and return before making investment
decisions.
10. Dashboard Interactivity
The dashboard includes:
• Dynamic slicers
• Cross filtering
• Drill-through pages
• Drill-down hierarchy
• Interactive tooltips
• Dynamic DAX measures
• Top N filtering
These features improve user experience and enable deeper data exploration.
11. Limitations
• Analysis is based on historical data and does not guarantee future returns.
• Market conditions may change over time.
• External economic factors are not included in the analysis.
12. Future Enhancements
Possible improvements include:
• Live mutual fund data integration using APIs.
• Portfolio recommendation system.
• Predictive return forecasting using Machine Learning.
• Benchmark comparison against market indices.
• Mobile-optimized dashboard.
• AI-powered investment recommendations.
13. Conclusion
This project successfully demonstrates how Python and Power BI can be combined to
analyze mutual fund performance and support investment decision-making. The
interactive dashboard enables users to compare funds across different return periods,
evaluate risk-adjusted performance, and explore insights using dynamic filtering, drill-
through, and cross-filtering features. The solution provides a user-friendly analytical
platform that helps investors identify high-performing mutual funds while considering
risk, expenses, and long-term consistency.
Dashboard Screenshots
