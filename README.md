# 8-Week-SQL-Challenge
# Case Study #1 - Danny's Diner
![1 (3)](https://user-images.githubusercontent.com/78970792/131291096-a6a7cd37-60cc-44fc-bd5e-50ef55c0eca7.png)
## Introduction
Danny seriously loves Japanese food so in the beginning of 2021, he decides to embark upon a risky venture and opens up a cute little restaurant that sells his 3 favourite foods: sushi, curry and ramen.

Danny’s Diner is in need of your assistance to help the restaurant stay afloat - the restaurant has captured some very basic data from their few months of operation but have no idea how to use their data to help them run the business.
## Problem Statement
Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite. Having this deeper connection with his customers will help him deliver a better and more personalised experience for his loyal customers.

He plans on using these insights to help him decide whether he should expand the existing customer loyalty program - additionally he needs help to generate some basic datasets so his team can easily inspect the data without needing to use SQL.

Danny has provided you with a sample of his overall customer data due to privacy issues - but he hopes that these examples are enough for you to write fully functioning SQL queries to help him answer his questions!
## Datasets
Danny has shared with you 3 key datasets for this case study:

**sales
menu
members**

## Entity Relationship Diagram
![Screenshot (148)](https://user-images.githubusercontent.com/78970792/131291531-df5c24a7-28bf-478e-8601-1828b7f228f3.png)
You can access it from this link:https://dbdiagram.io/d/608d07e4b29a09603d12edbd/?utm_source=dbdiagram_embed&utm_medium=bottom_open

## Table 1: sales
The sales table captures all customer_id level purchases with an corresponding order_date and product_id information for when and what menu items were ordered.
![Screenshot (150)](https://user-images.githubusercontent.com/78970792/131291789-7f6fa9ee-f659-481d-abcc-40dcd0e345ec.png)

## Table 2: menu
The menu table maps the product_id to the actual product_name and price of each menu item.
![Screenshot (152)](https://user-images.githubusercontent.com/78970792/131291883-2be9f3f1-aeca-45bc-8cd9-65c2c3166250.png)

## Table 3: members
The final members table captures the join_date when a customer_id joined the beta version of the Danny’s Diner loyalty program.
![Screenshot (154)](https://user-images.githubusercontent.com/78970792/131292005-40fa1e00-fb49-4f2f-885e-d9ae30276ff5.png)

# Case Study Questions Solutions
### 1.What is the total amount each customer spent at the restaurant?
I have applied inner join menu and sales table and applied aggregation sum to get the output and group by Customer_id
![Screenshot (157)](https://user-images.githubusercontent.com/78970792/131292607-ef5c28bf-cb1f-474c-b501-a2371bb8468c.png)

### 2.How many days has each customer visited the restaurant?
Count distinct order date can give me all customer visited dates without duplications
![Screenshot (163)](https://user-images.githubusercontent.com/78970792/131293071-59be7ad2-24f6-4d7f-9955-f26763d7cbd4.png)

### 3.What was the first item from the menu purchased by each customer?
Here atfirst I have applied  a simple window function dense_rank to get the order on the basis of order date and after that I have sorted them rank=1
and then after sorting I have applied again a rank on the basis of product id to get the first product of each customer
![Screenshot (168)](https://user-images.githubusercontent.com/78970792/131296603-0ab85006-a257-4182-9421-e55c2c0df34f.png)

### 4.What is the most purchased item on the menu and how many times was it purchased by all customers?
Here I have counted occurences of each product id and then ordered by descending and then by using join I have joined two tables and get the name of the proudct
and the occurence as well.
![Screenshot (171)](https://user-images.githubusercontent.com/78970792/131297188-eaf27496-5a6a-4570-8865-7b6e436c6c46.png)

### 5.Which item was the most popular for each customer?
Here atfirst I have counted the product id with group by customer id and then product id and then I have made a CTL(Common Table Expression)
and applied a windows function to get the ranks based on the occurences which named as "Pop" and then I have applied with clause to show the desired answer
![Screenshot (175)](https://user-images.githubusercontent.com/78970792/131298197-d17c1ebc-30c3-43ed-9a5c-6d489ce9bd93.png)

### 6.Which item was purchased first by the customer after they became a member?
Here atfirst I have used where clause and joins to get the data after the customer become a member and the ordered the data and I have used rank and CTL Concepts to 
get our desired output
![Screenshot (177)](https://user-images.githubusercontent.com/78970792/131298875-d752870b-54b9-4aa2-a0a6-e2d83ea1d421.png)

### 7.Which item was purchased just before the customer became a member?
Here atfirst I have used where clause and joins to get the data before they have joined and I have applied a CTL concept to get
our desired output
![Screenshot (179)](https://user-images.githubusercontent.com/78970792/131299168-62f36cef-bd87-4386-a785-cdeb34ee4154.png)

### 8.What is the total items and amount spent for each member before they became a member?
Here atfirst I have filtered the data before they have joined and then I have applied with and CTl Concepts to solve the problem
![Screenshot (181)](https://user-images.githubusercontent.com/78970792/131299689-b3ee96b9-5fe6-492c-8d7a-584e4310bb33.png)

### 9.If each $1 spent equates to 10 points and sushi has a 2x points multiplier - how many points would each customer have?
Here I have applied some conditions to get desired output
![Screenshot (184)](https://user-images.githubusercontent.com/78970792/131299976-74a6232e-2364-4ae3-bd8a-d53e4f41629d.png)

### 10.In the first week after a customer joins the program (including their join date) they earn 2x points on all items, not just sushi - how many points do customer A and B have at the end of January?
Here I have applied case statement for our desired output
![Screenshot (186)](https://user-images.githubusercontent.com/78970792/131300135-1c207919-8c38-4244-afb4-5a2604494e95.png)

