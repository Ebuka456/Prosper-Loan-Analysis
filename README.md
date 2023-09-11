# Prosper Loan Analysis: Who is struggling with their loans?

![](https://github.com/Ebuka456/Prosper-Loan-Analysis/blob/main/Property_Finance_Condo_Loan_sts_1372683893.jpg)

## INTRODUCTION
This project is dedicated to the analysis of a loan dataset from Prosper Loan, with the goal of gaining insights into customer borrowing behaviors. The primary objective is to enhance our understanding of customers and identify those who may be facing challenges in loan repayment.

This is the final project of the Udacity Data Analyst Nanodegree and this project helped me explore Data Visualization with Python for Exploratory and Explanatory Data Analysis.

### OVERVIEW OF THE DATASET

The dataset contains information of about 150K loaners that patronizes Prosper Loan. It 
has information about the loaners’ credit scores, loan status, employment status, 
occupation, amongst other variables. There are 81 fields for the dataset.


## DATA CLEANING
Using Feature Engineering to select the features most important for my analysis, I selected the columns below: 
- ListingKey: Unique key for each listing, same value as the 'key' used in the listing object in the API.
- ListingNumber: The number that uniquely identifies the listing to the public as displayed on the website.
- ListingCreationDate: The date the listing was created.  Term: The length of the loan expressed in months.
- LoanStatus: The current status of the loan: Cancelled, Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
- BorrowerAPR: The Borrower's Annual Percentage Rate (APR) for the loan.  ProsperScore: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score. Applicable for loans originated after July 2009.
- ListingCategory (numeric): The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans
- BorrowerState: The two letter abbreviation of the state of the address of the borrower at the time the Listing was created.
- Occupation: The Occupation selected by the Borrower at the time they created the listing.
- EmploymentStatus: The employment status of the borrower at the time they posted the listing.
- EmploymentStatusDuration: The length in months of the employment status at the time the listing was created.
- IsBorrowerHomeowner: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
- CurrentlyInGroup: Specifies whether or not the Borrower was in a group at the time the listing was created.
- TotalInquiries: Total number of inquiries at the time the credit profile was pulled.
- DebtToIncomeRatio: The debt to income ratio of the borrower at the time the credit profile was pulled. This value is Null if the debt to income ratio is not available. This value is capped at 10.01 (any debt to income ratio larger than 1000% will be returned as 1001%).
- IncomeRange: The income range of the borrower at the time the listing was created.
- StatedMonthlyIncome: The monthly income the borrower stated at the time the listing was created.
- LoanOriginalAmount: The origination amount of the loan.
- Recommendations: Number of recommendations the borrower had at the time the listing was created.

The full data cleaning and transformation steps was documented [here](https://github.com/Ebuka456/Prosper-Loan-Analysis/blob/main/Project_III_Part_I_Exploratory.ipynb)

### SUMMARY OF ANALYSIS

From the Analysis made, Here are the insights and conclusions I came up with:

1) There are 3 terms from the Dataset provided which are known by the number of 
months of the Loan. Term 12 which is for 12 months, Term 36 which is for 36 
months and Term 60 which is for 60 months.
- 77.04% of the Borrowers are in the Term 36
- 21.54% of them are in Term 60
- the remaining 1.42% are in Term 12

2) Though over 75% of the Borrowers are in the Term 36, Term 60 still has the highest 
Loan amount requested on average. Across all terms, Home Owners request for 
larger loan amount than Borrowers who are not loan Owners

3) Over 5000 of the Borrowers are still on the current loan while close to 4000 of them
have completed their loans. Almost 500 of them have defaulted

4) 2013 recorded the year with the highest number of Loan requests. January is the 
month of the year with the highest number of the loan requests.

5) The monthly Income of the borrower might affect their Loan status. The Borrowers 
who have Defaulted, Charged off and Cancelled all have a low average monthly 
income.

6) From the Loan status, there are more Borrowers in the Current Loan status but most 
of them are in the income range of $50000 - 74,999

7) The top Earning Occupation per month are Doctor, Attorney, Judge, Executive and 
Dentist. The least Earning Occupation are Students, Teacher, Waiter/Waitress, 
Nurses and Food Service.

8) According to investopedia, A general rule of thumb is to keep your overall debt-to-income ratio at or below 43%. Debt To Income ratio greater than 50% means that the borrower is not in a good place financially to take loan.
Using the benchmark of 50% for the Debt to Income ratio, we can see that all the 
borrowers in Term 60 and Term 12 do not exceed the benchmark which means that 
they are not struggling with their loan. In term 36, Borrowers that are Not 
Employed, Self Employed and Part time for their Employment status are the 
individuals who have thier average Debt to Income ratio above 0.5, therefore they 
mostly struggle with paying their loan

9) Using the benchmark of 50% for the Debt to Income ratio, The higher Debt to 
Income Ratio were observed for Borrowers that were Not Employed and Borrowers 
earning $1 - 24999. They are the group of Borrowers struggling with their loan

To view the full report for my insights, check [here](https://github.com/Ebuka456/Prosper-Loan-Analysis/blob/main/Project_III_Part_II_Explanatory.ipynb)

### KEY INSIGHTS

The main aim of the analysis is to observe the Borrowers (Loaners) and their general performance then 
look into which category of the loaners are struggling with their loan. 
From the Analysis, I used the 50% Debt to Income ratio to determine who was struggling with their loan. 
I discovered that the group of people who are struggling with their loan are mostly the Unemployed 
Loaners and Loaners with a low income range (less than $25,000). 
This serves the purpose of the analysis. 

### DATA VISUALIZATION
Data Visualization was done using Power BI. Find the Interactive report [here](https://app.powerbi.com/view?r=eyJrIjoiYzBjYjVmOGItMzhiZC00NDRjLTlhOTYtNzVkNGI0OWY3ODdiIiwidCI6IjUwZDA2MjZhLTcwN2UtNDk2ZC1iOGU1LTIwYjk1NzA5MTYzZSJ9)
![](https://github.com/Ebuka456/Prosper-Loan-Analysis/blob/main/Report%20Image/Prosper%20Loan%20Report_page-0001.jpg)
![](https://github.com/Ebuka456/Prosper-Loan-Analysis/blob/main/Report%20Image/Prosper%20Loan%20Report_page-0002.jpg)
