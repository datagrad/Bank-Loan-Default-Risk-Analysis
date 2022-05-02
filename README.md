# Bank Loan Default Risk Analysis

<a href="https://datagrad.github.io/"><img src="https://img.shields.io/badge/My%20Data%20Science%20Projects-Click%20here%20to%20Check%20my%20other%20Projects-blue">

With this case study, we aims to understand the strong driving factors behind <b>Loan Defaults</b>.

A loan lending company can use this case study to ensure that the consumers capable of repaying the loan are not rejected, and certain adaptable actions can be taken on client to basis if they are identified to face in difficulty paying their installments in future.

The result of this Risk analysis would help the bank to identify the patterns, which indicate if a client has difficulty paying their installments.

This can further influence the decisions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. 

<b> A Loan Lending Company can utilize this case adjective for its portfolio and risk assessment. </b>

## Business Understanding:
The primary business of any bank revolves around managing the spread between the deposits. In other words, when the interest that a bank earns from loans is greater than the interest it pays on deposits, it generates income from the interest rate spread.
  ![image](https://user-images.githubusercontent.com/73750698/141133748-8c0da7a3-489e-44f8-a36f-a8a3d59506b2.png)

<p align="center">
  <b>	
"The only good loan is one that gets paid back."
    </b>	
</p>

Clearly, the major part of revenues of any bank is attained through the loans they give to the people. But there are chances that the loans may not be paid back by few of the customers, making it a bad loan.

## Business Scenario:
When a customer applies for a loan, there are four types of decisions that could be taken by the customer/company:

<b>	1. Approved:  </b>	 The Company approved the loan Application.

<b>	2. Cancelled:   </b>	The client cancelled the application sometime during approval.

<b>	3. Refused:   </b>	The company rejected the loan.

<b>	4. Unused offer:   </b>	Loan has been cancelled by the client but on different stages of the process.


## Business Profitability:

The insufficient or non-existent credit history of an Urban Customer puts the bank lending company in position of dilemma about lending the loan.
This dilemma revolves around the likelihood that a customer would pay back the loan or not, and can potentially result in 2 types of loss:

<b>	1. Credit Loss:   </b>	If an applicant is not likely to repay the loan, then approving the loan may lead to a financial loss for the company.

<b>	2. Interest Loss:   </b> If an applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company.

![image](https://user-images.githubusercontent.com/73750698/141136353-e3fcfbfe-2ec4-4288-ba75-d8c2ee258f49.png)


# Approach:
## Dataset Information and overall data information check
We used two set of Datasets, 
1. application_data.csv, containing all the information of the client at the time of application. The data is about whether a client has payment difficulties. This further includes Data related to applicant’s socio economic status.
2. previous_application.csv contains information about the client’s previous loan data. It includes information that whether the previous application had been Approved, Cancelled, Refused or Unused offer.

## Data Cleansing
Next, we inititated the Data Cleansing process which included Null Value identification and strategic data modification, Data Type Conversion, and Outlier Treatment recommendation.
After we were confident of the data we had in hand, we wanted to analyse few numerical data after Binning them in acceptable intervals.

## Exploratory Data Analysis
We initiated the EDA process with a sole study of application dataset. It included <b> Univariate Analysis</b> , <b> Bivariate Analysis</b> , <b> Correlation Heat Map</b> , <b> Identification of top 10 most Correlated Variables</b>.

With this we targeted to identify the pattern and data of applications.

Next, we wanted to do a <b> Comparative Study</b>  between the current and previous application dataset. We started with merging both the dataset, and then analysed the variations.

Throughout the study, Defaulter collumn (variable) is used as target variable.

# Insights
![image](https://user-images.githubusercontent.com/73750698/141141851-1a53b254-aa7a-4274-9612-c978038adc49.png)
The ratio of Non-Defaulters to Defaulters is very high, giving Imbalance ratio of = .0878, because of this we used log scale to plot the curve to better understand the variations.


## Final Recommendations to Loan Lending Company
### **Likely Defaulter**
The Below listed Variables are potential identifier for a customer to be a **Likely Defaulter**
* Credit Score low External Source score
* Income: Range of 100000 to 200000
* Marital Status: Married, Single with high value loan, followed by Widows
* Education : Married , Highly educated with degrees, and high credit amount
* Number of Children 0 to 3 , High number of family members
* Occupation: Labourers , Sales Staff, Drivers , Managers, and Core Staff
* Lifestyle : Living in Own House, Apartments , Staying with parents, or owning a car
* Organization Small Businesses, Self employed, Small Traders, Persons in Medicine, Government, School applicants

### **Likely Non-Defaulter** 
The Below listed Variables are potential identifier for a customer to be a **Likely Non-Defaulter** 
* People with Higher Ext_Source_Score , especially EXT_SOURCE_3 score above 0.4, and EXT_SOURCE_2 score above 0.5
* People With Revolving Loans
* People who started their process over weekends. Those who initiated on Sunday are least like to default, followed by those who initiated on Saturday and then Friday.
* People with an income of 500000 and above, with their credit lying below 10000
* Businessman and Student from Name Income Type
* People who are accompanied by a group of people when came for taking a loan
* People with Academic Degree
* HR Staff, IT Staff, followed by Real state agents and private service staff
* People who own their own car and real estate
* People living in co operative or office apartment
* People with Unused offer in Name Contract Category
