# Amazon_Vine_Analysis

## Overview of the analysis of the Vine program
We have been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, we have access to 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. We’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the dataset.

This assignment consists of two technical analysis deliverables:
* 1: Perform ETL on Amazon Product Reviews.
Out of the 50 datasets, for the analysis I picked reviews that were given by the members for "Toys".
* 2: Determine Bias of Vine Reviews
I have used pyspark to determine Bias of Vine Reviews.

## Results:
* 1: Perform ETL on Amazon Product Reviews. 
 
I used PySpark to perform the ETL process to extract the "Toys" dataset. During data transformation, created four dataframes customers_table, products_table, review_id_table, and vine_table to better understand and analyze. Also, changed the datatype of review_date column from string to date.
Then established a connection to an AWS RDS instance and load the transformed data into pgAdmin.

![review_id_table](https://user-images.githubusercontent.com/111020934/204787026-89de83d0-5399-4e1e-aa5e-7c919ae4399c.PNG)


![products_table](https://user-images.githubusercontent.com/111020934/204787069-ca42f578-b183-42eb-8d88-50baebe50800.PNG)


![customers_table](https://user-images.githubusercontent.com/111020934/204787089-8b7adda2-4d25-4ad9-9580-4440114a3126.PNG)


![vine_table](https://user-images.githubusercontent.com/111020934/204787109-89e978d2-4d80-4448-9031-71191857e0e1.PNG)

* 2: Determine Bias of Vine Reviews

I have used pyspark to determine Bias of Vine Reviews.

1. How many Vine reviews and non-Vine reviews were there?

The count of vine reviews.
![image](https://user-images.githubusercontent.com/111020934/204788497-51ecb316-cd7e-4f88-b5d4-de66392e54bc.png)


The count of non-vine reviews.
![image](https://user-images.githubusercontent.com/111020934/204788785-09d3f2fd-e126-40a0-be02-dc593005748c.png)

The number of reviews by vine members is 1203 which is far less than non-vine members whose reviews count is 58018.


2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

![image](https://user-images.githubusercontent.com/111020934/204788987-07702a0f-3353-4d6d-909e-65a25592a8dc.png)


![image](https://user-images.githubusercontent.com/111020934/204789115-9301a14e-95e3-4f69-b26d-0d7b3cc81aa4.png)

The number of 5-star reviews by vine members is only 410 compared to non-vine members who have given 28043 5-star reviews.


3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

![image](https://user-images.githubusercontent.com/111020934/204790251-3b287a55-f238-45bd-981f-7cee1b29f4f2.png)

The percentage of 5-star reviews given by vine members is just 1.4% while by non-vine members is 98.6%

## Summary:

Based on the analysis we can state that there is no positivity bias for reviews in the Vine program.
The percentage of 5-star reviews given by the members of the vine program constitutes around 1.4% of the total 5-star reviews given.
This shows that the vine members are using the product to decide on posting a positive review instead of blindly giving a 5-star review and that they are showing no bias.
The rate at which the vine members are posting a review for a product must be compared with that of non vine members (review_date) that might support this statement.

Also, we need to extend our analysis for different datasets that might help us determine positive/negative Bias of Vine Reviews. We can also check if there is a bias of reviews for a product category/categories.















