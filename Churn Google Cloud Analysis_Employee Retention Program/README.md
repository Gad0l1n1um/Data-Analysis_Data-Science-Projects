# Employee Churn Prediction

## Problem Statement
This project aims to help identify employees who are likely to churn by building a predictive machine learning model.

## Approach
- We will use historical employee data to train an AutoML model using PyCaret.
- New employees in a pilot program will be tested with the model to predict their churn risk.

## Workflow
1. Build and manage a database in BigQuery.
2. Connect to the database using Python.
3. Train a churn prediction model using PyCaret.
4. Export predictions back to BigQuery.
5. Build a dashboard in Looker Studio for stakeholders to visualize insights.

Deliverable:
___________

Report/Dashboard

Analysis Questions
__________________

1. What is Causing Employees to Leave?

2. Who is Predicted to Leave?
  (highest probability to leave)

3. Are Employees Satisfied?

4. What Departments Have the Most Churn?


Project Questions
__________________

1. What Does Success Look Like?  Answer: A Higly Accurate Prediction Model.

2. What Does Failure Look Like?  Answer: An Inaccurate Model.

3. What Trends are Important?	 Answer: Features that are Causing Churn. e.g An employee that are causing them to leave.

4. What Actions Affect the Trend? Answer: What Recommendations can we Take.


DEVELOPING OUR MODEL
____________________

Machine Learning Workflow
-------------------------

Train			Test			Predict

Train Machine	      Test and Tune         Use the Optimized ML
Learning Model	     the ML Model for	    Model to predict which
on 70% of our	     Accuracy on the 	    employees in our pilot 
existing 15,000	     remaining 30%	    will Churn
employees																		


# CODE
_____

SQL - Merging the tables
-------------------------

SELECT *, "Orignial" as Type FROM `churn-cloud-project-437309.employeeData.tbl_hr_data`
UNION ALL
SELECT *, "Pilot" as Type FROM `churn-cloud-project-437309.employeeData.tbl_new_employees`


# CREDITS :

- FLATICON

- ABSENT DATA

# LICENSE

.gitignore