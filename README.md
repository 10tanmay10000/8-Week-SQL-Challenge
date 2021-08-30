# 8-Week-SQL-Challenge
# Case Study #1 - Danny's Diner
![1 (3)](https://user-images.githubusercontent.com/78970792/131291096-a6a7cd37-60cc-44fc-bd5e-50ef55c0eca7.png)
## Introduction
Danny seriously loves Japanese food so in the beginning of 2021, he decides to embark upon a risky venture and opens up a cute little restaurant that sells his 3 favourite foods: sushi, curry and ramen.

Danny’s Diner is in need of your assistance to help the restaurant stay afloat - the restaurant has captured some very basic data from their few months of operation but have no idea how to use their data to help them run the business.
# Problem Statement
Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite. Having this deeper connection with his customers will help him deliver a better and more personalised experience for his loyal customers.

He plans on using these insights to help him decide whether he should expand the existing customer loyalty program - additionally he needs help to generate some basic datasets so his team can easily inspect the data without needing to use SQL.

Danny has provided you with a sample of his overall customer data due to privacy issues - but he hopes that these examples are enough for you to write fully functioning SQL queries to help him answer his questions!
# Datasets
Danny has shared with you 3 key datasets for this case study:

sales
menu
members

# Entity Relationship Diagram
![Screenshot (148)](https://user-images.githubusercontent.com/78970792/131291531-df5c24a7-28bf-478e-8601-1828b7f228f3.png)
You can access it from this link:https://dbdiagram.io/d/608d07e4b29a09603d12edbd/?utm_source=dbdiagram_embed&utm_medium=bottom_open

# Table 1: sales
The sales table captures all customer_id level purchases with an corresponding order_date and product_id information for when and what menu items were ordered.
![Screenshot (150)](https://user-images.githubusercontent.com/78970792/131291789-7f6fa9ee-f659-481d-abcc-40dcd0e345ec.png)

# Table 2: menu
The menu table maps the product_id to the actual product_name and price of each menu item.
![Screenshot (152)](https://user-images.githubusercontent.com/78970792/131291883-2be9f3f1-aeca-45bc-8cd9-65c2c3166250.png)

# Table 3: members
The final members table captures the join_date when a customer_id joined the beta version of the Danny’s Diner loyalty program.
![Screenshot (154)](https://user-images.githubusercontent.com/78970792/131292005-40fa1e00-fb49-4f2f-885e-d9ae30276ff5.png)


