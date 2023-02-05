# Amazon_Vine_Analysis


## Overview

The purpose of this project was to analyze Amazon reviews written by members of the paid Amazon Vine program to submit to SellBy stakeholders. The Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review. Analysis on an apparel dataset was conducted to determine if there is any bias toward favorable reviews from Vine members. 

The apparel dataset was first imported into a Google colab notebook and read into a dataframe to prepare it for analysis. To pick reviews that were more likely to be informative the data was filtered into a new dataframe containing all rows where the total_votes count was greater than or equal to 20. Next, the data was filtered again into a new dataframe to find helpful reviews where the number of helpful_votes divided by total_votes was greater than or equal to 50%. The dataframe was then split depending on if the review was written as part of the Vine program (paid) or not part of the Vine program (unpaid). The values and percentages from each set of data was then used to make comparisons and determine if bias existed.


## Results

![Vine_df](https://github.com/Aleahkita/Amazon_Vine_Analysis/blob/main/Images/vine_reviews_df.png)

![Vine_results](https://github.com/Aleahkita/Amazon_Vine_Analysis/blob/main/Images/vine_results.png)

- There were 33 total Vine (paid) reviews
- Out of the total, 15 were 5-star reviews
- 45.45% of Vine reviews were 5-stars


![not_Vine_df](https://github.com/Aleahkita/Amazon_Vine_Analysis/blob/main/Images/not_vine_reviews_df.png)

![not_Vine_results](https://github.com/Aleahkita/Amazon_Vine_Analysis/blob/main/Images/not_vine_results.png)

- There were 45388 total non-Vine (unpaid) reviews
- Out of the total, 23733 were 5-star reviews
- 52.29% of Vine reviews were 5-stars


## Summary 

From the results, there does not seem to be bias for reviews in the Vine program. Comparing the percentages of 5-star reviews for each type, the percent of Vine 5-star reviews was lower than that of non-Vine reviews. While the percentage was slightly lower for the paid type of review it can also be noted that the percentages of 5-stars are not significantly different from each other, indicating a lack of bias from those in the paid Vine program. Another aspect to consider is the ratio of Vine vs non-Vine reviews in the dataset. Vine reviews accounted for 0.07% of the total reviews where non-Vine reviews accounted for 99.93%. 
Additional analysis that could be done to support these claims would be to expand the range of star-rating we analyzed. For example, we could look at reviews that got 4 and 5-star reviews as both are considered "positive", to see if there is a similar trend. We could also break down the reviews based on each rating from 1-5 and get counts and percentages based on the type of review to re-affirm our analysis. 
