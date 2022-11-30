# Retail_Customer_Segmentation_Sales_Prediction

## 1. Objectives

* Segment customers from a retail store based on their purchase behaviors on chocolate bars to help stakeholders conduct target marketing.

* Predict the price elasticity of purchase probability and quantity on various brands using linear regression, in order to assist marketers to make informed decisions.

* Formula: sales of a brand = probability of purchase * probability of choosing a brand * quantity * price.


## 2. Data 

The customer profile is comprised of 2000 customers with 7 features. The features include age, gender, marital status, education, income, occupation, settlement type.

<img src=https://user-images.githubusercontent.com/64850893/204099179-801a145c-fdc7-487a-8a34-5c3e044e04a6.png width="1000" height="500">

Reference: https://365datascience.com/courses/customer-analytics-in-python/


## 3. Methodology

* EDA
* Segmentation
* Modeling


## 4. EDA

* 4.1 Summary

<img src=https://user-images.githubusercontent.com/64850893/204099649-036f6ca3-edad-473a-85da-fdbf8ea3aab1.png width="700" height="300">


* 4.2 Correlation

<img src=https://user-images.githubusercontent.com/64850893/204099812-60b34f8c-b773-4d95-b778-ffe8a393bf1f.png width="600" height="300">


## 5.Segmentation

* 5.1 Hierarchical Clustering

<img src=https://user-images.githubusercontent.com/64850893/204100040-ba139006-46d6-4ca5-a35e-f2f8ece21294.png width="600" height="300">


* 5.2 K-means

<img src=https://user-images.githubusercontent.com/64850893/204100134-bfbbdcfe-dff4-4401-bd93-5067af2d812f.png width="600" height="400">


* 5.3 PCA

<img src=https://user-images.githubusercontent.com/64850893/204145810-6d258edd-d406-4ada-a11f-2bb8e0d37452.png width="600" height="400">


* 5.4 K-means & PCA

<img src=https://user-images.githubusercontent.com/64850893/204145780-322c980b-c5e5-433b-a3ba-fb389e8326c5.png width="600" height="400">

** We can observe that the clients are fairly separated with K-means and PCA.

** The 4 segments are named based on the level of income and age.

## 6. Purchase Data Analytics

* 6.1 Segment Proportion:

<img src=https://user-images.githubusercontent.com/64850893/204149152-9ce089b6-b63b-4725-a5f9-a0260b465bd3.png width="500" height="400">

** Note: segment 0 - Standard, segment 1 - Career-Focused, segment 2 - Fewer-Opportunities, segment 3 - Well-Off.


* 6.2 Number of Purchases by Segment:

<img src=https://user-images.githubusercontent.com/64850893/204149392-b59755b3-bb74-4729-8353-dfdf90865f1e.png width="600" height="400">


* 6.3 Brand Choice by Segment

<img src=https://user-images.githubusercontent.com/64850893/204149427-8e633251-8887-4671-9606-2e0e71d4d8d3.png width="600" height="400">


* 6.4 Revenue by Segment

<img src=https://user-images.githubusercontent.com/64850893/204149477-dc490236-22a7-4ca2-8c80-2f6b7b796167.png width="1000" height="300">


## 7. Price Elasticity of Purchase Probability

* Ultilize linear regression to predict the purchase probability.

* Compute the probability by 4 segments and plot:

<img src=https://user-images.githubusercontent.com/64850893/204606176-3c7ce5f4-3009-44ed-b461-e8cbd293690a.png width="600" height="500">

** Note: grey (overall), blue (segment 0 - Standard), green (segment 1 - Career-Focused), red (segment 2 - Fewer-Opportunities), orangle (segment 3 - Well-Off).

* We observe that the Well-off (orange) segment are the least elastic when compared to the rest. So, their purchase probability elasticity is not as affected by price.

* The price elasticities for the Standard (blue) segment seem to differ across price range. This may be due to the fact that the Standard segment is least homogenous, which we discovered during our descriptive analysis. It may be that the customers in this segment have different shopping habits, which is why their customers start with being more elastic than average but then shift to being more inelastic than the average customer.


## 8. Price Elasticity of Purchase Probability with and without Promotion

* Compute the price elasticity of purchase probability with and without promotion, then plot:

<img src=https://user-images.githubusercontent.com/64850893/204611399-4e744aef-f1bf-454e-a270-4b5e091dbf2e.png width="600" height="500">

** Note: blue (without promotion), red (with promotion).

* Here we observe that the purchase probability elasticity of the customer is less elastic when there is a promotion.

* This is an important insight for marketers, as according to our model, people are more likely to buy a product if there is some promotional activity rather than purchase a product with the same price, when it isn't on promotion. 

## 9. Brand Choice

<img src=https://user-images.githubusercontent.com/64850893/204612941-89eb8024-fdd2-41ed-aab9-96abd7ceed51.png width="700" height="500">

* The 2 segments, which seem to be of most interested for the marketing team of brand 5, appear to be the Career-focused and the Well-off. They are also the segments which purchased this brand most often.

* The Career-focused segment is the most inelastic and they are the most loyal segment.

* Based on our model, they do not seem to be that affected by price, therefore brand 5 could increase its price, without fear of significant loss of customers from this segment.

* The Well-off segment, on the other hand, seems to be more elastic. They also purchase the competitor brand 4 most often. In order to target this segment, the related price needs to be decreased. However, keep in mind that other factors aside from price might be influencing the purchase behaivour of this segment.

## 10. Price Elasticity of Purchase Quantity with and without Promotion

<img src=https://user-images.githubusercontent.com/64850893/204656387-3ceb326f-ca54-4a94-a9ab-1601e41d2f2a.png width="700" height="500">

* The 2 elasticities are very close together for almost the entire price range.

* It appears that promotion does not seem to be a significant factor in the customers' decision on what quantity of chocolate candy bars to purchase.

## 11. Takeaways

* Customers are segmented into 4 groups based on their demographics and purchased behaviors.
* The Well-off segment is the least elastic in terms of purchase probability, compared to the other groups.
* The purchase probability elasticity of the customers is less elastic when there is a promotion, which means people are more likely to buy a product if there are some promotional activities.
* The Career-focused segment is the most inelastic and the most loyal segment. Therefore, brand 5 could increase its price, without fear of significant loss of customers from this segment.
* Promotion does not impact the customers' decision significantly on what quantity of chocolate candy bars to purchase.
