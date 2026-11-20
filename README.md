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

Using PNC Payment Data to Improve Account Verification
PNC’s verification team explored how to supplement Early Warning data with its own payment records and micro-deposit results to improve coverage and client confidence.
Current verification gaps and proposed direction
Verification Services primarily relies on Early Warning Services (EWS) for account status and ownership checks; gaps in its data can leave clients without a useful answer.
The product team wants to use PNC’s data to reduce those gaps, beginning with PNC accounts and ownership matching, then potentially extending to accounts supported by transaction history.
Micro-deposit verification is being developed as a fallback: a penny transaction carries a six-digit code that the recipient confirms through a client-branded email or text experience.
The micro-deposit project is being fast-tracked using agentic development; the team was about 40 days into a 90-day build window. Commercial launch is not guaranteed by day 91.
The proposed longer-term approach could combine EWS, PNC records, and other data sources, with a normalized client-facing result rather than a more complex set of statuses.

Data analysis, matching, and risk considerations
A retrospective analysis would compare client inquiry inputs and EWS responses with PNC’s contributed data as of the time of each inquiry.
PAI records the inquiry inputs and raw EWS outputs. PNC account or contribution history would need to come from historical Hogan or other core tables, with timing aligned to what EWS likely held at the time.
The analysis should test EWS name-matching behavior without assuming it is always correct; prior work found cases where transaction names appeared to match but EWS returned a mismatch.
Any PNC matching rules would need to account for recency, transaction frequency, returns, and fraud indicators. Current account status may be more informative than older data contributed to EWS.
Chris said the client terms pass through the information-only and liability limitations in PNC’s EWS agreement. He noted that misunderstandings can occur when an account appears to exist but ownership is unconfirmed.
EWS charges $0.55 per payment-check inquiry and an additional $0.55 for an AOA match when ownership data is available. PNC currently pays EWS for inquiries about PNC accounts whose data PNC contributed.

Micro-deposits and virtual accounts
Micro-deposits could create reusable verification evidence, subject to a defined validity period; the team discussed possible shelf lives but made no decision.
EWS does not currently support virtual account numbers. PNC’s Virtual Account Management product maintains a crosswalk between supported virtual accounts and underlying DDAs, though virtual-account schemes vary across banks.
Chris’s view was that transaction history could help validate a virtual account even without identifying it as virtual, if payments to that identifier repeatedly completed without issue.

Planning and delivery
The team did not set a production date for the data-driven verification work. Chris hopes to make progress in 2027, subject to engineering capacity and approvals from business, risk, legal, and other PNC stakeholders.
The product team expects micro-deposit launch in the first quarter of next year.
Direct front-end engineering support was not considered necessary at this stage; the team highlighted the need for standardized statuses and response translation.

Action items
Send the presentation deck to the team.
Use the planning meeting in about two weeks to map the work, estimate duration, and update Chris on priorities and needs.

