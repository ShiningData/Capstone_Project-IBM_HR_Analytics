Automating the Reg E International Payments Compliance Tracker
The session reviewed a spreadsheet-based Reg E monitoring process for international retail payments and outlined requirements gathering as the first step toward an automated dashboard.
Current Reg E monitoring and compliance review
Monitoring scope: Quarterly review tracks outgoing international retail payments, destination institutions and countries, and fee disclosures; the process could run monthly or on demand.
Reg E threshold: The analysis identifies SWIFT BICs and checks whether the annualized payment count reaches the 500-payment threshold (501 or more), which informs whether an institution-country combination remains in scope.
Compliance review: Payment records are matched with fee-type data to identify cases where a fee could be deducted. GOR indicates Bank of America guarantees no fee deduction; other fee types receive review notes to distinguish disclosure issues from non-issues.
Manual spreadsheet work: The tracker combines SQL output, PRS data, and a weekly Bank of America lifting-fee file. Numerous formulas, XLOOKUPs, copy-and-paste steps, and pivot tables make the workbook slow and difficult to train others to maintain.
Annual reporting: The process supports reporting the number and total dollar value of payments with guaranteed no-fee treatment versus payments where a fee could be deducted. One cited figure was $2 billion in USD or USD-equivalent payments over the first three quarters of the year.
Operational trends and analysis in the tracker
Channel adoption: Since PNC introduced international payments through retail mobile and web, usage has shifted from branch initiation to digital channels. About 70% of international retail payments now go through retail mobile; initially, about 70% were initiated through branches.
Payment growth: Comparing Q1 2022 with Q1 2026, payment volume had nearly doubled.
Returns: The tracker began including returns last year. Q1 2025 had 845 returns, or about 2%; the current rate was described as a little over half a percent, indicating improved payment quality.
Additional breakdowns: Pivot tables summarize payment counts by country and currency, payments above or below $10,000, completed versus returned payments, and return counts or rates. Mexico ranked highest by return count, while lower-volume countries such as Ireland could have higher return rates.
Data-quality follow-up: A New Zealand-dollar return entry looked unusual and needs checking.
Data sources and automation approach
Payments Engine: The main payment data comes from a SQL query against the Payments Engine database; migration to COD was raised as a possible way to run it for the automated solution.
PRS: The SWIFT-code reference data may be available directly from the PRS database. The process owner recently received access to run Oracle queries there and will ask the PRS team about extracting the required information.
Lifting-fee file: The Bank of America file contains fee types and SWIFT IDs. Multiple rows can exist per BIC because of fee amount tiers; the current workflow removes duplicates because the analysis needs fee-type codes rather than fee amounts.
Requirements before implementation: The process owner will document each step, its source data, field meanings, calculations, and aggregations. The initial scope will prioritize understanding and assembling core data; the additional pivot-table outputs can be addressed later.
Dashboard direction: Scott agreed the work could be a candidate for a Streamlit-based dashboard, subject to reviewing the requirements and clarifying open questions. The stated goal was to have a dashboard before the end of the year.

Action items
Megan: Share the spreadsheet and prepare requirements describing the core data sources, fields, calculations, and process steps by Friday as far as possible; prioritize the core data before documenting the additional pivot tables.
Megan: Ask the PRS team whether the required reference information can be queried or extracted from the PRS database.
Scott: Review the requirements, explore a Streamlit sketch, raise clarification questions, and arrange a follow-up meeting; begin work toward a dashboard before the end of the year.



# Capstone_Project-IBM_HR_Analytics

## Introduction
Attrition, in Human Resource terminology, refers to the phenomenon of the employees leaving the company. Attrition in a company is usually measured with a metric called attrition rate, which simply measures the no of employees moving out of the company (voluntary resigning or laid off by the company).   
 
In this project, we want to predict the attrition of the company’s valuable employees, uncover the factors that lead to employee attrition.

## Project Proposal
The problem and approach to solve the problem in project proposal. You can click [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Project%20Proposal/Capstone%20Project%20Proposal.pdf) to reach it.

## Data
I use IBM HR Analytics Employee Attrition & Performance data from Kaggle, which is created by IBM data scientists. Dataset is in the open source website and can be reached from this [link](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/tree/master/data). It has 1470 rows x 35 columns and contains numeric and categorical data types in columns. I loaded the dataset from this link in csv format and read it in the Jupyter notebook after importing necessary libraries.

## Data Wrangling
Data wrangling notebook and report can be reached form this [link](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/tree/master/Data_Wrangling) 

## Exploratory Data Analysis
Univarate and bivariate analysises are done by using bar charts and heatmap visualizations. These analysis can be found [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Exploratory%20Data%20Analysis/Exploratory%20Data%20Analysis%20Notebook.ipynb)

## Hypothesis Test
Inferential statistics notebook can be reached [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Inferential%20Statistics/Inferential%20Statistics%20-%20IBM_HR_Analytics.ipynb)


## Interim report 
Interim report can be found [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Capstone%20Project%20Interim%20Report/Capstone%20Project%20Mid-Report.pdf)

## Modeling
This is a supervised binary classification problem. We used Python’s Scikit Learn libraries to solve the problem. In this context, we implemented Logistic Regression, Decision Tree, Random Forest, K-NN, SVM, Kernel SVM, Naive Bayes, Gradient Boosting, and AdaBoosting algorithms. We applied hiperparameter tuning, PCA, and SMOTE techniques to the algorithms. 

Modeling notebooks can be reached from following [link](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Machine_Learning/HR%20Analytics%20Employee%20Attrition%20and%20Performance.ipynb)

## Conclusion
Final report can be found [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Milestone_Report/Final%20Capstone%20Project%20Report%20.pdf)

Project Presentation can be found [here](https://github.com/ShiningData/Capstone_Project-IBM_HR_Analytics/blob/master/Milestone_Report/Capstone%20Project%20Presentation.pptx)

