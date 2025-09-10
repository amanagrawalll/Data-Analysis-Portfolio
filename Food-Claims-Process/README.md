# Case Study Project - Food Claims Process

## Company Background

Vivendo is a fast food chain in Brazil with over 200 outlets. As with many fast food
establishments, customers make claims against the company. For example, they blame
Vivendo for suspected food poisoning.
The legal team, who processes these claims, is currently split across four locations. The new
head of the legal department wants to see if there are differences in the time it takes to close
claims across the locations.

## Customer Question

The legal team has given you a data set where each row is a claim made against the
company. They would like you to answer the following questions:

- How does the number of claims differ across locations?
- What is the distribution of time to close claims?
- How does the average time to close claims differ by location?

The dataset needs to be validated based on the description below:

|Column Name          |Criteria                                                                                                                             |     
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------|  
|Claim ID             |Character, the unique identifier of the claim.                                                                                       |
|Time to Close        |Numeric, number of days it took for the claim to be closed.                                                                          |
|Claim Amount         |Numeric, initial claim value in the currency of Brazil. For example,“R$50,000.00” should be converted into 50000.                    |
|Amount Paid          |Numeric, total amount paid after the claim closed in the currency of Brazil.                                                         |
|Location             |Character, location of the claim, one of “RECIFE”, “SAO LUIS”,“FORTALEZA”, or “NATAL”.                                               |
|Individuals on Claim |Numeric, number of individuals on this claim.                                                                                        |
|Linked Cases         |Binary, whether this claim is believed to be linked with other cases, either TRUE or FALSE.                                          |
|Cause                |Character, the cause of the food poisoning injuries, one of ‘vegetable’, ‘meat’, or 'unknown’. Replace any empty rows with ‘unknown’.|


## Data Discovering and Visualization

### How does the number of claims differ across locations?

For a better understanding of the number of claims across the four locations, a bar plot becomes useful. As we see, Sao Luis has the highest number of Claims and Natal has the lowest number of Claims.

![claims_per_location](https://user-images.githubusercontent.com/56371747/200199208-29f32bb8-4f3b-4258-9d84-69e651c53f8f.png)


Then when comparing the number of Claims; specifically, Sao Luis has 38% more claims with respect to Natal

![df_claims_diff](https://user-images.githubusercontent.com/56371747/200199224-6d031ccd-9f5d-4aa5-b40b-2a27125e75d8.png)


### What is the distribution of time to close claims?

To see a Distribution the histogram is a useful visualization. The next bar plot is the first data visualization to demonstrate the characteristic of time to close variable.

![time_close_dist](https://user-images.githubusercontent.com/56371747/200199235-2340dc8e-15be-4c3a-a1f2-cb47b3b15f5b.png)


The distribution of Time to Close Claims is a "Right Skewed" also known as a positively skewed histogram, that can be verified by its Mean > Median > Mode. Then a box plot could add more information about the Range of Time to Close a Claim by finding its Intequantile Range.

This next box plot represent the second data visualization to demonstrate the characteristic of Time to Close variable.

![time_close_boxplot](https://user-images.githubusercontent.com/56371747/200199254-c86e1937-c247-4681-aaf5-5966f2470f50.png)

The Interquartile Range for the Time to Close a Claim across all four Locations is between 349 and 1143 days. However, it must be remembered that the highest number of Claims is at Sao Luis.


### How does the average Time to Close Claims differ by Location?

The highest average Time to Close a Claim (1063 days) is at Sao Luis, and the lowest average Time to Close a Claim (581 days) is at Natal. As shown:

![avg_time_per_location](https://user-images.githubusercontent.com/56371747/200199268-0c1c0c31-1e48-4d9b-82f6-3153de8f3338.png)

Even though the highest average of Time to Close a Claim is at Sao Luis, the averages of Time to Close (green triangles) for Fortaleza and Recife are affected by their outliers, forcing them to augment and get close to the average Time to Close of Sao Luis.

This is the data visualization to demonstrate the relationship between Time to Close per Location variables:

![dist_time_across_locations](https://user-images.githubusercontent.com/56371747/200199289-6008fdcb-2a05-493f-9ab0-aea05750adab.png)


Fortaleza, Recife and Natal's Average Time to Close a Claim are lower when removing outliers. As shown:

![dist_time_across_locations_no_outliers](https://user-images.githubusercontent.com/56371747/200210601-b56b5c00-0e3c-4a01-8723-c7d8d733609b.png)

As we observe, after removing outliers the averages of Time to Close in Recife, Fortaleza and Natal get even lower than the average of Time to Close in Sao Luis. Thus, the most appropiate comparison would be without outliers

Sao Luis the highest number of Claims, 52%  more claims with respect to Natal, which has the lowest number of Claims. Besides, the average Time to Close a Claim is 134% more in SAO LUIS in comparison with NATAL. This could be due to SAO LUIS having a larger Interquartile Range and a larger Whisker in comparison with the other Locations and without considering the outliers in Fortaleza, Recife and Natal.

![df_avg_time_diff_no_outliers](https://user-images.githubusercontent.com/56371747/200220049-1ab1a0a0-1683-452a-bd9e-2619bc9186f4.png)



## Summary

- Sao Luis has the highest number of Claims (29), and the highest Average Time to Close too (1063 days).

- Natal has the lowest number of Claims (19) and also the lowest Average Time to Close (456 days).

- At Sao Luis, Claims take 134% of more days to close in comparison with Natal, which has the lowest days to close a Claim. Furthermore, Sao Luis has 52% of more claims with respect to Natal.






































