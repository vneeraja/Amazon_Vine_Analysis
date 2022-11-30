# Amazon_Vine_Analysis

## Overview of the analysis of the Vine program
We have been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, we have access to 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. We’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in the dataset.

This assignment consists of two technical analysis deliverables:
*1: Perform ETL on Amazon Product Reviews.
Out of the 50 datasets, for the analysis I picked reviews that were given by the members for "Toys".
*2: Determine Bias of Vine Reviews
I have used pyspark to determine Bias of Vine Reviews.

## Results:
*1: Perform ETL on Amazon Product Reviews. 
 
I used PySpark to perform the ETL process to extract the "Toys" dataset. During data transformation, created four dataframes customers_table, products_table, review_id_table, and vine_table. Also, changed the datatype of review_date column from string to date.
Then established a connection to an AWS RDS instance and load the transformed data into pgAdmin.

![review_id_table](https://user-images.githubusercontent.com/111020934/204787026-89de83d0-5399-4e1e-aa5e-7c919ae4399c.PNG)

![products_table](https://user-images.githubusercontent.com/111020934/204787069-ca42f578-b183-42eb-8d88-50baebe50800.PNG)

![customers_table](https://user-images.githubusercontent.com/111020934/204787089-8b7adda2-4d25-4ad9-9580-4440114a3126.PNG)

![vine_table](https://user-images.githubusercontent.com/111020934/204787109-89e978d2-4d80-4448-9031-71191857e0e1.PNG)
