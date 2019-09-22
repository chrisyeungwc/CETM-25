# CTEM-25 Data Visualisation

Introduction: As a data visualiser in a data scientist start-up company, you are tasked to design and develop a bespoke Big Data visualisation product as part of an individual R & D project. 
The viewer of your data visualisation product will be those junior governmet officals who have no or very limited knowlegde of data scuence or data visualisation rechnologies, but need to install, deploy, and use your data visualisation product to visualise a compelling data storytelling for a group of targeted audiences who are professional data driven journalists of public media.

## Open Dataset
This is a dataset from Kaggle, [**Lending Club Loan Data**](https://www.kaggle.com/wendykan/lending-club-loan-data).

### Description
The file "loan.csv" contains open loan data from [**Lending Club**](https://www.lendingclub.com/company/about-us) in US. 
The period covered from Jun2007 to Dec2018. The loan data only includes the successful loan applications but not rejected applications. 
Dataset has 145 columns, which involves different types of information such as annual income, credit grade, loan purpose etc. 
It is noted that there is no leakage of personal information, such that the readers do not know the loan applicants. 

### Data Pre-processing and Cleansing
The dataset used in dashboard has been modified.

* New update data 2019Q1 and 2019Q2 has been downloaded from [**Lending Club**](https://www.lendingclub.com/company/about-us).
* Anthoer dataset "state.csv" is uploaded to convert the abbreviation of states to be full name.
* Column "term" is changed to be numeric format.
* A new column "loan_int" is derived by "int_rate" * "loan_amnt".
* A new column "year_quarter" contains the year and quarter of the loan issued date "inssue_d".
* A new column "bad_loan" contains the loan may be potentially default or default already, which the loan status includes “Charge Off”, “In Grace Period”, “Late Payments” and “Default”.
* A new column "total_int" means the total interests from the loans, i.e. "installment" * "term" - "loan_amnt".
* A new column "region" contains five regions, West, South West, South East, Mid West and North East.
* A new column "income_cat" contains three income categories, 1) Low income category: Borrowers that have an annual income lower or equal to USD100,000; 2) Medium income category: Borrowers that have an annual income higher than USD100,000 but lower or equal to USD200,000; 3) High income category: Borrowers that have an annual income higher tha USD200,000.

## Code Style 
This data visualisation programming language is R and development platform is R Studio. The source code has been uploaded as CETM25.Rmd. 

## Built With
* The dashboard is built by flexdashboard R Markdown file. 
* [**Demostration**](https://chris-yeung.shinyapps.io/CETM25/) is uploaded to [**shiny.io**](https://www.shinyapps.io/).  
