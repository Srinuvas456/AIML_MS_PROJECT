# Lending Club Case Study
> Lending Club is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures.

## Business Scenario and Risks Involved
> When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. 
> Two types of risks are associated with the bank’s decision:
> * If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

> *If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company
## Table of Contents
* [Problem Statement] (#problem-statement)
* [General Info] (#general-information)
* [Conclusions] (#conclusions)
* [Technologies Used] (#technologies-used)
* [Acknowledgements] (#acknowledgements)
<!-- You can include any other section that is pertinent to your problem -->

## Problem Statement
### Business Understanding
When a person applies for a loan, there are two types of decisions that could be taken by the company:

Loan accepted: If the company approves the loan, there are 3 possible scenarios described below:

* Fully paid: Applicant has fully paid the loan (the principal and the interest rate)

* Current: Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.

* Charged-off: Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan

Loan rejected: The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### Business Objectives

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). 
Credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.

The company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## General Information
- Steps for EDA :
<ol>
    <li>Data Understanding</li>
    <li>Data Cleaning</li>
    <li>Univariate Analysis</li>
    <li>Bivariate Analysis</li>
    <li>Multivariate Analysis</li>
    <li>Conclusion</li>
</ol>
- Data Set : Loans.csv 
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
<div class="alert alert-block alert-danger">
    <span style='font-family:Georgia'>
        <b>Driving Factors for Loan Defaults : </b> <br><br>
        <b>Continuous Variable: </b>
        <ol>
		<li>Loan Amount:  Loan amount higher than 10000$ has more default percentage</li>
            <li>Interest Rate:  Higher interest rates show higher loan defaults.<br>
            <li>Annual Income: Lower annual incomes(up to 10K) shows higher loan defaults (up to 25%)</li>
			<li>Installments:  Higher loan installments (between 600$ to 1200$) cause loan defaults.</li>
            <li>DTI: DTI ratio higher than 10 witnesses more loan defaults (14-16%).</li>
        </ol>
        <b>Categorical Variable : </b>
        <ol>
            <li>Term: 60 months have more loan defaults in comparison to 36 month term.</li>
			<li>Purpose: Small business owners are more likely to commit frauds.</li>
            <li>Grade: As the grade decreases (from A to G) default percent increases, customers with lower grades and subgrades are a risk.</li>
            <li>VERIFICATION STATUS :  Verified customer are more prone to charge off (loan default)</li>
            <li>STATE : Percent of loan defaulted is very high for state NE and high for NV and SD</li>
        </ol>
    </span>    
</div>


<div class="alert alert-block alert-success">
    <span style='font-family:Georgia'>
        <b>Recommendations:</b> 
        <ul>
            <li>Lending Club should be cautious before approving any loans above 15000$</li>
            <li>If interest rate is higher, loan defaults are higher, consider approving loans at lower interest rates and low loan amounts.</li>
            <li>Lower annual income and higher DTI are a risk, avoid such applicants to reduce credit loss.</li>
            <li>Small business owners and 60 month loan terms are risk areas, should minimise these applicants.</li>
            <li>Applicants with lower grade and subgrade(D2-G5) should not be considered for loan approvals.</li>
            <li>Verified borrowers are causing more credit loss, update customer verification process.</li>
	    <li>Loan Applications of customers having grades in A1-C3 are less likely to be defaulted.
        </ul>
    </span>    
</div>

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- pandas - 1.3.5
- matplotlib - 3.2.2
- seaborn - 0.11.2
- plotly - 5.8.0

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- https://seaborn.pydata.org/
- https://plotly.com/
- https://pandas.pydata.org/
- https://learn.upgrad.com/

## Contact
Created by [@Srinuvas456]


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->

