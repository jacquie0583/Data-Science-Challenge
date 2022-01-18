# Data-Science-Challenge
Summer 2022 Internship Program
# Question 1: Given some sample data, write a program to answer the following: click here to access the required data set
https://docs.google.com/spreadsheets/d/16i38oonuX1y1g7C_UAmiK9GkY7cS-64DfiDMNiR41LM/edit#gid=0

On Shopify, we have exactly 100 sneaker shops, and each of these shops sells only one model of shoe. We want to do some analysis of the average order value (AOV). When we look at orders data over a 30 day window, we naively calculate an AOV of $3145.13. Given that we know these shops are selling sneakers, a relatively affordable item, something seems wrong with our analysis. 


Think about what could be going wrong with our calculation. Think about a better way to evaluate this data. 
Possibly the incorrect AOV calcuations are due to the calculating the tital_items with the aggregate, count(),function instead of sum().  With the count()function provides the number of rows, sum() allows for adding of the values in the total_items colums.

What metric would you report for this dataset?
The Average Order Value metric is the sum of both 'order_amount' and 'total-amount', as follows:

oa_sum = data_df['order_amount].sum()
ti_sum = data_df['total_itmes'].sum()
Then,
AOV = oa_sum/ti_sum
What is its value?
AOV = $357.92
 
