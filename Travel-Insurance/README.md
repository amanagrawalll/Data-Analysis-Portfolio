# Case Study Project - Travel Insurance

## Company Background

Travel Assured is a travel insurance company. Due to the COVID pandemic, they have had to cut their marketing budget by over 50%. It is more important than ever that they advertise in the right places and to the right people.

Travel Assured has plenty of data on their current customers as well as people who got quotes but never bought insurance.

## Customer Question

They want to know:
- Are there differences in the travel habits between customers and non-customers?
- What is the typical profile of customers and non-customers?

## Business goal

Increase customer attraction by identifying where the most potential customer are.

## How the Data Analysis address the business problem?

By answering the business customer questions:

By answering **Are there differences in the travel habits between customers and non-customers?**, I would find differences in travel habits between customers and non-customers I might feedback to the marketing department with descriptive statistics data so they could re-adjust and therefore keep an eye on the target for the advertising.

*It's important to note the Travel Habits from the Dataset:* Frequent Flyer, Ever Traveled Abroad and Travel Insurance

When I answer **What is the typical profile of customers and non-customers?**, the marketing department has descriptive data around the customer and non-customer profiles, they could define the patterns of non-customers to develop marketing strategies and in consequence discover paths to reach non-customer preferences.


## Dataset

**1987 rows, 9 columns**

|Column Name           |Details                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------|  
|Age                   |Numeric, the customer’s age.                                                                                  |
|Employment Type       |Character, the sector of employment.                                                                          |
|Graduate Or Not       |Character, whether the customer is a college graduate into.                                                   |
|Annual Income         |Numeric, the customer’s yearly income.                                                                        |
|Family Members        |Numeric, the number of family members living with the customer.                                               |
|Chronic Diseases      |Numeric, whether the customer has any chronic conditions.                                                     |
|Frequent Flyer        |Character, whether a customer books frequent tickets.                                                         |
|Ever Travelled Abroad |Character, has the customer ever travelled abroad.                                                            |
|Travel Insurance      |Numeric, whether the customer bought travel insurance.                                                        |



## Data Discovering and Visualization

### Are there differences in the travel habits between customers and non-customers?

Yes, I found differences between customers and non-customers, in a travel habits context. Remebering that the three Travel Habits are Frequent flyer, Ever traveled abroad, adn Travel insurance. First of all, I found that there are more Non-Customers than Customers, knowing that Customer is a traveler that has ever bought an insurance once in his lifetime, as the ratio show:

![customersvsnoncustomers](https://user-images.githubusercontent.com/56371747/203883457-235c50dd-ba97-49cf-bf3e-216065f5c144.png)


Talking about if there are more Customers or Non-Customers being Frequent flyer or Not. I found more Non-Frequent flyers for both categories, but I found that Customers are more Frequent flyer than Non-Customers as we can see:

![frequentflyers](https://user-images.githubusercontent.com/56371747/203885787-cdaf6648-156e-4bb0-ba62-a661efe3dcb7.png)


About if travelers have ever Traveled abroad I found that for both Customers and Non-Customers there are more travelers that never traveled abroad, nevertheless, there are way more Customers Travelers that ever Traveled abroad than Non-Customers that ever Traveled abroad:

![traveledabroad](https://user-images.githubusercontent.com/56371747/203885796-9fc25bfc-25c1-4ba3-a22c-ebec055405c6.png)



### What is the typical profile of customers and non-customers?

In the case of the profiles of Customers and Non-Customers, the age distribution looks similar between them. The average Age for both is 30 years old:

![agedistribution](https://user-images.githubusercontent.com/56371747/203887538-0c7e109c-12fa-47bf-adb3-c644ac3f3331.png)


For the Employment type both Customers and Non-Customers work in Private Sector/Self Employed type, but there more Non-Customers that work in Government Sector:

![employmenttype](https://user-images.githubusercontent.com/56371747/203887780-a647b159-c007-4aad-8227-bbcd3b6ddea8.png)


If Customers or Non-Customers are Graduated or not, I found a very similar proportion between being Graduated or Not:

![graduatedornot](https://user-images.githubusercontent.com/56371747/203887923-c65d7404-30fe-4800-9e78-120d10d7722a.png)


I found a very interesting Annual income distribution between Customers and Non-Customers, for Customers their Annual income is 37.8% more than for the Non-Customers:

![annualincome](https://user-images.githubusercontent.com/56371747/203888117-dd6c46b2-06a1-4e23-bce6-f14f3964e5c5.png)


The number Family members distribution is very similar for both Customers and Non-Customers, finding an average of 4 Family members between them:

![familymembersdistribution](https://user-images.githubusercontent.com/56371747/203888230-8478ed54-3413-4118-ae2d-9024b9b70d49.png)


Treating Customers and Non-Customers having Chronic disease, have a very similar proportion prevailing that having not Chronic disease:

![chronicdiseases](https://user-images.githubusercontent.com/56371747/203888532-d820f0c8-c4b6-4a49-b7d8-c15a9b28a5d5.png)


## Conclusions

### Differences in travel habits between customers and non-customers:

- Even though 36% of the travelers are customers, 34% of those customers are frequent flyers versus only 14% of non-customers are frequent flyers.

- Talking about if travelers have ever traveled abroad, it have been found that 42% of the customers have traveled abroad once time, meanwhile just 6% of non-customers have ever traveled abroad.


### Typical profile of customers and non-customers

|Customers                                               | Non-Customers                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------|
|36% of Travelers are Customers (710 Travelers).         |64% of Travelers are Non-Customers (1277 Travelers).                    |
|34% are Frequent flyers.                                |14% are Frequent flyers.                                                |
|42% have Traveled abroad.                               |Just 6% have ever Traveled abroad.                                      |
|Average age are around 30 years old.                    |Average age are around 30 years old.                                    |
|80% of customers work in Private Sector/Self Employed.  |66% of Non-Customers work in Private Sector/Self Employed.              |
|86% of Customers are Graduated.                         |85% of Non-Customers are Graduated.                                     |
|Mean Annual income is 1.13 million dollars. (37.8% more non-customer average annual income)            |Mean Annual Income of 0.82 million dollars.                             |
|Average Family Members is 4 members.                    |Average Family Members is 4 members.                                    |
|71% of Customers have no chronic disease.               |73% of Non-Customers have no chronic disease.                           |


## Recommendations

There is a negative highly correlated relationship (left side) between the Annual Income (independent variable) and the Average Age (dependent variable), thus the recommendation is to offer Travel Insurance to potential customers who follow the trendline above. The probability of Travel Insurance acceptance would increase if these potential customers follow the profiles described in the past slide. On the right side, I found that there is no relationship between de Annal income and the Average Age for Non-Customers.

![age_vs_annual](https://user-images.githubusercontent.com/56371747/203897408-ef45e89b-2902-4a99-8b1d-99a644b9e9b3.png)


In another hand, has been found a negative highly correlated relationship (right side) between Annual income and the quantity of Non-Customers. This means that Non-Customers with lowest Annual incomes found expensive the plans or cannot pay the prices of Travel insurance. The recommendation is to offer basic Travel insurance for those who have the lowest Annual income, and the points described in the Customer profile. On the left side, we see that there is no relationship between the Number of Customers and their Annual income.

![qtynoncustomers_vs_income](https://user-images.githubusercontent.com/56371747/203897414-92b1ea22-6b99-4460-8bf7-a7fa1cce6fd9.png)














