# Loan Default Prediction model based on Lending Club Data

Lending Club is a US-based fintech company that offers P2P lending platform.
In this project, I have analysed a subset of the Lending Club data available on Kaggle(https://www.kaggle.com/wordsforthewise/lending-club)
The dataset I have used(lending_club_loan_two.csv -which is the data and lending_club_info.csv -which is information about the columns) is a subset of the dataset in the above link and has additional information added to make it more usable.

## About the data
LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC), and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform. Here are the considerations when lending to borrowers:
1. loan_amnt	The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
2. term	The number of payments on the loan. Values are in months and can be either 36 or 60.
3. int_rate	Interest Rate on the loan
4. installment	The monthly payment owed by the borrower if the loan originates.
5. grade	LC assigned loan grade
6. sub_grade	LC assigned loan subgrade
7. emp_title	The job title supplied by the Borrower when applying for the loan.*
8. emp_length	Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years.
9. home_ownership	The home ownership status provided by the borrower during registration or obtained from the credit report. Our values are: RENT, OWN, MORTGAGE,    OTHER.
10. annual_inc	The self-reported annual income provided by the borrower during registration.
11. verification_status	Indicates if income was verified by LC, not verified, or if the income source was verified
12. issue_d	The month which the loan was funded
13. loan_status	Current status of the loan
14. purpose	A category provided by the borrower for the loan request.
15. title	The loan title provided by the borrower
16. zip_code	The first 3 numbers of the zip code provided by the borrower in the loan application.
17. addr_state	The state provided by the borrower in the loan application
18. dti	A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income.
19. earliest_cr_line	The month the borrower's earliest reported credit line was opened
20. open_acc	The number of open credit lines in the borrower's credit file.
21. pub_rec	Number of derogatory public records
22. revol_bal	Total credit revolving balance
23. revol_util	Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.
24. total_acc	The total number of credit lines currently in the borrower's credit file
25. initial_list_status	The initial listing status of the loan. Possible values are – W, F
26. application_type	Indicates whether the loan is an individual application or a joint application with two co-borrowers
27. mort_acc	Number of mortgage accounts.
28. pub_rec_bankruptcies	Number of public record bankruptcies

## Data Preparation
1. Cleaning and feature engineering i.e removing and substituting null values, irrelevant features, converting categorical features to dummy variables and extracting useful features from the available features.
2. Visualisations using Matplotlib and Seaborn to understand the data and the features and understand the correlations with the label.
3. Data is normalised using MinMaxScaler since it is passed through a Deep Learning Model.

## Deep Learning Model
1. Created a Deep Learning Model using Keras API of Tensorflow.
2. Added dropout layers to avoid overfitting.

## Model performance is evaluated using sklearn metrics
It performs comparitively poorly on f1 score since the classes are unbalanced. The model can be improved by treating the unbalanced classes and fine tuning the hyperparameters of the model.
