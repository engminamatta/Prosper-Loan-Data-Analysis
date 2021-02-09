# Prosper Loans data analysis
to download CSV file, Please click the follwoing link:
https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv

#Dataset

>This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

-A number of characteristics about Prosper loans in each raw:
>-    LoanStatus:	The current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted,
        FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket. 
    BorrowerAPR:	The Borrower's Annual Percentage Rate (APR) for the loan.
    BorrowerRate:	The Borrower's interest rate for this loan. 
    LenderYield:	The Lender yield on the loan. Lender yield is equal to the interest rate on the loan less the servicing fee.
    EstimatedEffectiveYield:	Effective yield is equal to the borrower interest rate (i) minus the servicing fee rate, (ii) minus estimated uncollected interest on charge-offs, (iii) plus estimated collected late fees.  Applicable for loans originated after July 2009.
    ProsperRating (Alpha):	The Prosper Rating assigned at the time the listing was created between AA - HR.  Applicable for loans originated after July 2009.
    ProsperScore:	A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009.
    ListingCategory:	The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans
    EmploymentStatus:	The employment status of the borrower at the time they posted the listing.
    CurrentCreditLines:	Number of current credit lines at the time the credit profile was pulled.
    DebtToIncomeRatio:	The debt to income ratio of the borrower at the time the credit profile was pulled. This value is Null if the debt to income ratio is not available. This value is capped at 10.01 (any debt to income ratio larger than 1000% will be returned as 1001%).
    IncomeRange:	The income range of the borrower at the time the listing was created.
    IncomeVerifiable:	The borrower indicated they have the required documentation to support their income.
    TotalProsperLoans:	Number of Prosper loans the borrower at the time they created this listing. This value will be null if the borrower had no prior loans. 
    LoanOriginalAmount:	The origination amount of the loan.
    MonthlyLoanPayment:	The scheduled monthly loan payment.
    Recommendations:	Number of recommendations the borrower had at the time the listing was created.


>The follwoing questions are required here to investigate this dataset:
   What factors are important for us to predict if a loan will be completed or defaulted?


#Key Insights for Presentation:

In this analysis I used some features to show their effect on Loan completion.
so I made analysis of every feature of the previous mentioned featrures against (Loan status)
I used mainly boxplots, violin plots histograms  and countplots. 
I used these plots beacause I was investigating the loan status which is categorical against many nnumerical quantitive variables.

# Summary of Findings

What factors are important for us to predict if loan will be completed or not?.
Results:
>We can notice that "HR" category is the greater one to cancel loan
>D category is the most probable to complete loan
>For category (1) completed, Full time is the largest factor for loan completion
>A slight notice here that deafaulted loans tend to have higher lender yield, 
or by other words for low lender yield it is better predicted for the loan to be completed
>Most of Borrower APR values is between 0 - 0.2 in completed loans
>For cancelled loans most of borrower APR values is between 0.1 - 0.3
i.e. we think the lower the APR the bigger te chance to complete Loan
>Defaulted loans are concentrated in the first two categories(NotAvailable, Debt consolidation)
where 1 = Debt Consolidation and 7 = other
so Debt Consolidation is the most listed loan category to be completed
>For those who were defaulted the largest count has no cateogry available which needs more investigation from propser.
>Past due category has higer Monthly loan Payment than completed loans, also cancelled ones have lower than completed.
>Recommendation didn't make a difference
>No of Loans didn't make any difference either
