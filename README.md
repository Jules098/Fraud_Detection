# Mini-project IV

### [Assignment](assignment.md)

## Project/Goals
The goal of this project is to create a machine learning model that will take a loan applicant's information and predict whether or not a loan will be approved.
The algorithm will then be deployed to the cloud using Flask.

## Hypothesis
Null hypothesis: Applicants with higher incomes and a credit history will have their loans approved more often.  The more income they can fall back on, the lower the likelihood of default, and the safer it is for the bank to grant the loan.

## EDA 
During the exploratory data analysis, two things stood out:

1. The largest gap that existed between approved or not approved in any variable was higher income co-applicant income.  Applicants with higher co-applicant income were rejected far more regularly than not.
2. The vast majority of the loans were of a term-length of 15 years or more.


## Process
(fill in what you did during EDA, cleaning, feature engineering, modeling, deployment, testing)
### Step 1: Check for missing values.
### Step 2: Split the numerical and categorical variables
### Step 3: Move Loan_Amount_Term and Credit_History to categorical variable dataframe.  Switch their values to str equivalents.
### Step 3: Derive the rate of appearance for each categorical variable (57% of applicants had no dependets, 8% had 3+, etc.)
### Step 4: Create visualizations to view distributions and relationships between both the numerical and categorical data.
### Step 5: Impute missing values.  LoanAmount was imputed with the mean of loans given.  Categorical variables with more than 5% of their data missing were imputed with a randomly selected set of NaN rows that reflected the proportion in which each variable appeared in the total dataframe (84% of applicant's had credit history, so 84% of all NaN values in credit history were given yes randomly, etc.)  All variables with less than 5% of their data missing had their rows with null values dropped.
### Step 6: Numerical Data was log transformed to deal with outliers.
### Step 7: Cleaned dataframe finalized, train test split on the cleaned dataframe.
### Step 8: Created the predictive model using pipeline.
### Step 9: Fit and Predict the pipeline with Gradient Boosting Classifier
### Step 10: Use GridSearch to get the best parameters.
### Step 11: Get predict score.


## Results/Demo
(fill in your model's performance, details about the API you created, and (optional) a link to an live demo)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time? are there any potential issues/biases with your model/use case?)
