# Marketing-Campaign-Analysis_SQL-Project
To work on some of the pain points of the marketing team to help them work on new set of campaigns or doing market basket analysis.

### Project Overview
- XYZ Paints Inc. is a paint company which was recently launched in 2019. Since then, they have established their name in top tier 1 and 2 cities, they are seeing quite steady growth so slowly expanding to tier 3 cities as well. 
- They have given a sample of data from their databases. You have to work on some of the pain points of the marketing team like consumer growth, lead conversions, etc. as well as help them work on new set of campaigns or doing market basket analysis.

### Data Source
Data Tables were on the Metabase
Data Schema is shared below.

 ![image](https://github.com/user-attachments/assets/c6cf89e8-8f3a-4c34-947c-c5a629d72ee6)

### Data Handling
Project taskes are divided into the five sections -

# Section - 1 Getting the overview of the data
  
Q1. Check the cardinality of following columns:
Different color segments (categories) provided by the company.
Different Coupon Types that are offered.
States where the company is currently delivering its products and services.
Different Order Types.

Q2. Identify total number of sales (transactions) happened by
Yearly basis
Quarterly basis
Yearly and Monthly basis

Q3. Identify the total purchase order by
Product category
Yearly and Quarterly basis
Order Type
City Tier

# Section - 2 Understanding lead conversion

The company wants to understand the customer path to conversion as a potential purchaser based on the campaigns.
1. Identify the total number of transactions with campaign coupon vs total number of transactions without campaign coupon.
2. Identify the number of customers with first purchase done with or without campaign coupons.
3. Identify the impact of campaigns on users.
a. Check the total number of unique users making purchases with or without campaign coupons.
b. Check the purchase amount with campaign coupons vs normal coupons vs no coupons.

Based on the above analysis, make a comment on whether or not the campaigns were effective overall in driving the customers towards our brand or not.

# Section - 3 Understanding company growth and decline

The marketing team is interested in understanding the growth and decline pattern of the company in terms of new leads or sales amount by the customers.
1. Identify the total growth on an year by year basis excluding the current year
a. Based on quantity of paint that is sold
b. Based on amount of paint that is sold
c. Based on new customers that are acquired. (Hint: Get distinct new users every year before year by year analysis).
     i. Segregate them By OrderType (Note: This is a new question, sub-part of 1c)

All the results should be in one single record except last part of 1.c. Please make an analysis of what is happening with our customer acquisition and sales growth over the years.
1, Identify the total decline, if any, within the total sales amount on an year by year basis excluding the current year. Comment on whether we need to launch a campaign for the consumers based on the recent pattern. What campaign type will be more appropriate for this scenario out of all the predefined distinct campaign types? [Note: Unlike previous question, get all the results for different years in their own records]

# Section - 4 Market basket analysis

A market basket analysis is defined as a customer’s overall buying pattern of different sets of products.
Essentially, the marketing team wants to understand customer purchasing pattern. Their proposal is if they promote the products in their next campaign, which are bought couple of times together, then this will increase the revenue for company. 
Please answer the following questions:
1. Please identify the dates when the same customer has purchased some product from the company outlets. Transactions from same order types and different products are only valid transactions here. [Hint: A Special type of Joins is required on customer id and exclude the exact same transactions.]
2. Out of the above, please identify the same combination of products coming at least thrice sorted in descending order of their appearance. 
3. Out of the above combinations (coming thrice), please check which of these combinations are popular in different sectors (household, industrial and government).

On the basis of above three, please highlight the combinations of products that are bought couple of times in data on the same day. Also, comment on which combinations should be promoted/advertised together to these different sectors.

# Section - 5 Automating tasks

Company is thinking of launching a new campaign in upcoming months. Please automate the following tasks.

1. Create Functions for the following:
Get the total discount, if any. 
Get the days/month/year elapsed since the last purchase of a customer depending on input from user. [Hint: Use If condition within the function]
2. Create Views (using above functions) for the following:
a. Identify the top 10 customers along with their demographic details from each sector based on their total discount.
b. Identify the top 5 customers (from household and industrial sector) based on purchase amount and days elapsed in descending order. Do highlight if you think there is a data error.
c. Identify the top 10 products that are sold last year based on sales amount along with the last 2 year details of the same. 
d. Create 3 different income groups for household sector people - ‘high class’, ‘low class’, ‘middle class’ - based on their percent rank (33% each) and identify the top 2 products that are bought within these income class.

3. Create Stored Procedures for following data validation tasks:
Identify whether a particular transaction amount (purchase amount) is ‘correct’ or ‘not correct’. 
It is correct if price and quantity are used to calculate without a coupon. In case of a coupon, the coupon amount should be deducted from the original amount given the original amount is greater than equal to min purchase for a coupon; else you can simply calculate original amount based on quantity. 
[Input will be transaction id] [Note: Look out for null coupon ids]
Check if there is any customer with age < 12. Print out the total such customers on-screen.


