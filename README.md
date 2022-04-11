## Amazon_Vine_Analysis
# Overview

In this repository, an analysis was completed for Amazon reviews written by members of the paid Amazon Vine program for Camera product listings on the Amazon commerce platform. The Amazon dataset's ETL process and Analysis was completed using PySpark in Google Colab where the transformed data was loaded to a local postgreSQL database with an AWS RDS instance. The data was analyzed to identify any potential bias toward favorable reviews from Vine members. 

# Results 

1. Dataframes were created to prepare for loading.
![image](https://user-images.githubusercontent.com/95376544/162662370-89877ea5-32da-454e-97f0-f58f7d37c7e9.png)

2. Connection to the AWS RDS Instance was created and each Dataframe was written to its table.
![image](https://user-images.githubusercontent.com/95376544/162663104-77b87038-295a-4802-8f71-bcf07449c52f.png)

3. The dataset was filtered to create dataframes that identified the counts of reviews for different metrics.
![image](https://user-images.githubusercontent.com/95376544/162663386-e3bb25fd-d2dc-4beb-b905-3836d417c2f0.png)

# #We can use these dataframes to answer these questions!

* How many Vine reviews and non-Vine reviews were there?

There were 607 Vine reviews and 50522 non-Vine reviews.

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

There were 257 5-star Vine reviews and 25220 5-star non-Vine reviews.

* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

42.3% of Vine reviews were 5-stars and 49.9% of non-Vine reviews were 5 stars. 

# Summary

There does not appear to be a bias from Vine reviewers as there is a lower percentage (42.3%) of their reviews showing favor with 5-star reviews, whereas non-Vine reviews (49.9%) show more favor towards these products. We would be able to identify potential bias even easier since the sample size of the Vine reviews are significantly smaller compared to the non-Vine reviews that are showing a larger percentage of 5-star reviews. To identify if there is bias from Vine reviews vs non-Vine reviews, the same analysis could be done on another dataset for a different product category.
