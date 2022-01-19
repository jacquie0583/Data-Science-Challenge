# Data-Science-Challenge
Summer 2022 Internship Program
#  Question 1: Given some sample data, write a program to answer the following: click here to access the required data set
https://docs.google.com/spreadsheets/d/16i38oonuX1y1g7C_UAmiK9GkY7cS-64DfiDMNiR41LM/edit#gid=0

On Shopify, we have exactly 100 sneaker shops, and each of these shops sells only one model of shoe. We want to do some analysis of the average order value (AOV). When we look at orders data over a 30 day window, we naively calculate an AOV of $3145.13. Given that we know these shops are selling sneakers, a relatively affordable item, something seems wrong with our analysis. 


#  a.  Think about what could be going wrong with our calculation. Think about a better way to evaluate this data. 
Possibly the incorrect AOV calcuations are due to the calculating the total_items with the aggregate, count(),function instead of sum().  With the count()function provides the number of rows, sum() allows for adding of the values in the total_items colums.  Other influences like outliers and faulty data could have affected on the metric.

#  b.  What metric would you report for this dataset?
Once the outliers are removed the reason for the skewed data becames apparent.  So the median becomes a solid meteric; wanting to use multiple metrics the interquartile range and the the average value per each store.  The latter explains the revenue numbers per each store per month and it shows the stores with the outliers.  Historical data can provide insight as to the stores' revenue and see if numbers increased or decreased with the previous time periods. 

The Average Order Value metric is the sum of both 'order_amount' and 'total-amount', as follows:

oa_sum = data_df['order_amount].sum()
ti_sum = data_df['total_itmes'].sum()
Then,
AOV = oa_sum/ti_sum
#  c. What is its value?
AOV = $357.92

<p align="center">
  <img width="200" height="200" src="https://github.com/jacquie0583/SQL-Challenge---Case-Study-/blob/main/Picture2.png">
</p>
 
#  Question 2: For this question you’ll need to use SQL. Follow this link to access the data set required for the challenge. Please use queries to answer the following questions. Paste your queries along with your final numerical answers below.

How many orders were shipped by Speedy Express in total?
What is the last name of the employee with the most orders?
What product was ordered the most by customers in Germany?
