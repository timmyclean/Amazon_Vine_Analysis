# Amazon_Vine_Analysis

## Overview of Analysis
* We have been tasked with analyzing the Amazon Vine Program which "allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review."
* We were asked to look at our choice of data set provided Amazon. The product we chose was "Shoes".
* We used Pyspark to perform the ETL process and extract, transform, connect to an AWS RDS instance and then load in to pgAdmin.
* We then used pandas to determine if there is a bias toward favorable reviews from Vine members in our "Shoe" dataset.

## Results

### Questions

1- How many Vine reviews and non-Vine reviews were there?
   * Customers who recieved products (shoes) through the Vine program that had 50% higher correlation with the "helpful_vote" and "total_vote" columns was 22 as seen by the following images;
![image](https://user-images.githubusercontent.com/76462602/115123381-c2f3e880-9f8a-11eb-892d-d586be31e382.png)
![image](https://user-images.githubusercontent.com/76462602/115123397-dd2dc680-9f8a-11eb-8a3e-e6a074dfb7d7.png)

  * Customers who were independent of Vine Program with same parameters of 50% higher correlation with the "helpful_vote" and "total_vote" columns was 26,987 a  much larger pool as seen by following images;
![image](https://user-images.githubusercontent.com/76462602/115123517-60e7b300-9f8b-11eb-91bc-a308d6761fde.png)
![image](https://user-images.githubusercontent.com/76462602/115123535-79f06400-9f8b-11eb-906e-b922edeca3cd.png)

2- How many Vine and Non-Vine reviews were 5 Stars?
  * of the 22 Vine reviews 13 were 5 star
![image](https://user-images.githubusercontent.com/76462602/115123647-03a03180-9f8c-11eb-97dc-a02070bbf5f4.png)

  * of the 26,987 Non-Vine reviews 14,475 were 5 star 
![image](https://user-images.githubusercontent.com/76462602/115123666-187cc500-9f8c-11eb-8c30-7267e946d150.png)

3- What percentages of Vine and Non-Vine reviews were 5-Stars?
  * Vine = 59% 
![image](https://user-images.githubusercontent.com/76462602/115123736-65f93200-9f8c-11eb-839f-5223cfffd4fa.png)
  * Non-Vine = 54%
 ![image](https://user-images.githubusercontent.com/76462602/115123761-7f01e300-9f8c-11eb-99fb-196bf39dfc14.png)

## Summary

  * When looking at the results we have concluded that there is not a positivity bias when analyzing the Vine program. Although we also have concluded that it may not be as beneficial compared to just letting "true" customers provide feedback. Especially in the case of "shoes" individuals feet are very different. 
  * Additional analysis we would look at would be the total reviews not just the reviews with a 50% or higher correlation. 
  * Also we look at a comparison of specific shoes that have been reviewed by both Vine and Non-Vine customers
