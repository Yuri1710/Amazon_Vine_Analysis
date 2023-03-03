# Amazon_Vine_Analysis

## Objective

1. Define big data and describe the challenges associated with it.
2. Define Hadoop and name the main elements of its ecosystem.
3. Explain how MapReduce processes data.
4. Define Spark and explain how it processes data.
5. Describe how NLP collects and analyzes text data.
6. Explain how to use AWS Simple Storage Service (S3) and relational databases for basic cloud storage.
7. Complete an analysis of an Amazon customer review.

We touch three main topics in these challenge:

+ **Hadoop Distributed File System (HDFS)** 
+ **MapReduce** 
+ **Yet Another Resource Negotiator (YARN)** 

## Resources

- Datasets:

  - US Apparel dataset
  - Technologies used:

- Google Colab (to run PySpark)
  - Jupyter Notebook
  - AWS S3 and RDS
  - PostgreSQL

Determine Bias of Vine Reviews
Using PySpark we have extracted the same dataset in a new Google Colab Notebook Vine_Review_Analysis.ipynb . We have recreated the vine_table and we have performed the following steps:

Created a new DataFrame to retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors.

Filtered the new DataFrame and created a new DataFrame to retrieve all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%.

Filtered the later DataFrame and created a new DataFrame or table that retrieves all the rows where a review was written as part of the Vine program/paid, and another one where the review was not part of the Vine program/unpaid.

![Capture](https://user-images.githubusercontent.com/114257085/222611911-1f777728-6f80-4a1b-8972-e5afd5b93d29.PNG)

![image](https://user-images.githubusercontent.com/114257085/222612093-c6107ab2-437d-4638-93a0-36cdb940ce2a.png)

![Capture](https://user-images.githubusercontent.com/114257085/222612323-750fdd3b-1131-45b9-8ffe-dfcd08eea034.PNG)

![Capture](https://user-images.githubusercontent.com/114257085/222612432-7e56bc2f-4f71-4d49-91db-d8345f2eb842.PNG)

## Summary

In conclusion, the vine program might just not be worth it for the apparel category. As it can be seen, there were not many helpful reviews that made part of it (total of 33), and only around half of them were 5-star rated (45%). Very similarly to the unpaid reviews which also only half of them were 5 star rated (52%). Even though the percentages may be misleading as the volume of reviews in the vine and non-vine programs vary so much, this itself is a sign that the vine program is not very popular in this category. We might not want to pay for it as it is not incentivizing the people to write better reviews.

This allows us to conclude that customers don't feel a positivity bias for leaving good reviews in the paid program as there are so few and not so many well-rated. Nevertheless, if we were to further analyze we could calculate the mean of the star ratings on each programs' reviews to see if there's a significant incentive.




