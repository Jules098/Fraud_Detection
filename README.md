# Mini-project IV - Fraud Detection

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
- Move Loan_Amount_Term and Credit_History to categorical variable dataframe.  Switch their values to str equivalents.
- Derive the rate of appearance for each categorical variable (57% of applicants had no dependets, 8% had 3+, etc.)
### Step 3: Create visualizations to view distributions and relationships between both the numerical and categorical data.
### Step 4: Impute missing values.  
- LoanAmount was imputed with the mean of loans given.  
- Categorical variables with more than 5% of their data missing were imputed with a randomly selected set of NaN rows that reflected the proportion in which each variable appeared in the total dataframe (84% of applicant's had credit history, so 84% of all NaN values in credit history were given yes randomly, etc.)  All variables with less than 5% of their data missing had their rows with null values dropped.
### Step 5: Numerical data was log transformed to deal with outliers.
### Step 6: Cleaned dataframe finalized, train test split on the cleaned dataframe.
### Step 7: Created the predictive model using pipeline.
- Fit and Predict the pipeline with Gradient Boosting Classifier
### Step 8: Use GridSearch to get the best parameters.
- Get predict score.
### Step 9: Deploy Machine to the cloud.


## Results/Demo
My model's performance was not strong.  The predictive scores were 72% while running the gridsearch somehow dropped the scores to 64%.  Somewhere I made a mistake although at this point it's difficult to assess where that was.

## Challenges 
Correctly imputing the missing values for Credit History and Self-Employment were difficult.  The other big difficulty was deploying the project to the cloud.  There are still a number of steps that I don't have written down that I should.

## Future Goals
In the future, I would like to spend more time running tests to better test my null hypothesis.
