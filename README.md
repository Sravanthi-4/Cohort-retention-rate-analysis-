# Cohort-retention-rate-analysis-  
For any business it is important to use a data driven approach to build a stratergy to undersatnd customers and target them. For a medium to large size retail store, it is also imperative that they invest not only in acquiring new customers but also in customer retention. Many businesses get most of their revenue from their best or high-valued customers who are loyal and keep coming back. It is equally important to find the customers who are at high risk of churning. The aim of the project is to group similar customers into groups called cohorts based on a certain condition.  

## Cohort analysis
Cohort analysis is an analytical technique that aims at analysing groups based on some common behavioural trait over a certain period of time or in certain location. This technique is generally used to better understand the cohorts, and improve user retention.  

Break down of customers into cohorts can be done in two ways:
-  Aquisition cohorts: divides users based on the time one signed up/ got a product.
- Behavioural cohorts: divides users based on actions taken by them over a specific period of time.

Firstly, the necessary libraries are imported. The required data for the project is downloaded from Kaggle and is also provided in this repository. The dataset is obserevd to undersatnd different aspects of the features/variables. The labels customer id and descriprtion are obsered to have few null or missing values.

### Cleaning the data
The rows with duplicate values are deleted.  As the customer id is required to group the customers in later steps, the rows with missing customer id are removed. Then the clean data is used to perform cohort analysis.  

For cohort analysis few new lables are created from the existing ones:
-Invoice period: A string representation of the year and month of a single transaction/invoice.
-Cohort group: A string representation of the the year and month of a customer’s first purchase. This label is common across all invoices for a particular customer.
-Cohort Index: A integer representation a customer’s stage in its lifetime. The number represents the number of months passed since the first purchase.

### Types of cohorts
Time Cohorts: The customers who signed up for a product or service during a particular time frame are put in same group.
Behaovior cohorts: The customers who purchased a product or subscribed to a similar service in the past are grouped together.
Size cohorts: It refer to the various sizes of customers who purchase company’s products or services. This categorization can be based on the amount of spending in some periodic time after acquisition or the product type that the customer spent most of their order amount in some period of time

Aquisition based time cohort table is made by grouping active customers in each cohorts on monthly basis. From this table retantion table is build in precentages which represents the retention rate. Retention measures how many customers from each of the cohort have returned in the subsequent months.
For better understanding this table is represented using heatmap. 
