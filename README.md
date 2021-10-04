# Amazon_Vine_Analysis
## Overview of the Analysis 
Since our work with Jennifer on the SellBy project was so successful, we've been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

We were given access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I have chosen to focus this analysis on the furniture reviews dataset. I used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I used PySpark to determine if there is any bias toward favorable reviews from Vine members within the chosen dataset.

## Results 
Using the Vine Table created in Deliverable 1 we first filtered for 20 or more total votes and where the percent of helpful votes/ total votes was greater than or equal to 50%. 

1. How many Vine reviews and non-Vine reviews were there?\
Of our filtered dataset there were 18,155 total reviews (18019 unpaid and 136 paid).

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?\
Of our filtered dataset there were 8,556 5-Star Reviews. (8482 unpaid and 74 paid). 

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?\
47% of the unpaid reviews were 5-Stars while 54% of the paid reviews were 5-Stars.  

## Summary 
The 7 percentage point difference in percent positive reviews may suggest that gifting Vine members products to review does create a positive bias in their reviews. We would want to conduct a probability test to determine whther this difference is statisitcally significant. We may also want to replicate our analysis on another amazon dataset to see if our finding are consistent across products. 
