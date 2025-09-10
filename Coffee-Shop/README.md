# Case Study Project - Coffee Shops

## Company Background

Caffeine Form is a company creating coffee cups from recycled material. Although they
started selling the products on their website last year, the results were not as good as they
expected. To better enter the market, they decided to collaborate with local coffee shops to
advertise and sell their coffee cups.

The marketing team is trying to come up with the best criteria to choose possible
collaborators by investigating the local market. They think focusing on the places with the
most reviews might have the biggest impact as more good reviews will create more
excitement for their cups.

## Customer Questions

They would like you to answer the following questions to help:

- What is the most common place type in this local market?
- How does the range in number of reviews differ across all shops?
- How does the number of reviews vary across each place type?

The dataset needs to be validated based on the description below:

|Column Name    |Criteria                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------|
|Region         |Character, one of 10 possible regions (A to J) where coffee shop is located.                                  |
|Place name     |Character, name of the shop.                                                                                  |
|Place type     |Character, the type of coffee shop, one of “Coffee shop”, “Cafe”,“Espresso bar”, and “Others”.                |
|Rating         |Numeric, coffee shop rating (on a 5 point scale).                                                             |
|Reviews        |Numeric, number of reviews provided for the shop. Remove the rows if the number of reviews is missing.        |
|Price          |Character, price category, one of “$”, “$$” or “$$$”.                                                         |
|Delivery option|Binary, describing whether there is a delivery option, either True or False.                                  |
|Dine in option |Binary, describing whether there is a dine-in option, either True or False. Replace missing values with False.|
|Takeout option |Binary, describing whether there is a takeout option, either True or False. Replace missing values with False.|


## Solution

### What is the most common place type in this local market?

To find the most common place type, a good way is using histograms based on the count of each type of places

![most_common_place_type](https://user-images.githubusercontent.com/56371747/198067516-d08bca02-a1b6-4b3a-aef6-f431c5a549e5.png)


As the histogram shows, the Coffee Shop type is the most commonplace. Then the Marketing Team must aim their efforts to sell to this type of place.




### How does the range in the number of reviews differ across all shops?

Again, the histogram is good view of the frequency of Reviews

![num_reviews_across_all_shops](https://user-images.githubusercontent.com/56371747/198424188-195532fb-d876-4390-ba1f-6bcc42b5f40e.png)


As the plot show, a few local coffee shops with almost 3000 reviews were found, these are considered outliers and were excluded.

A boxplot could clarify the threshold of the reviews to take in consider

![num_reviews_across_all_shops_2](https://user-images.githubusercontent.com/56371747/198439610-07710b7d-a78a-47ad-9ad7-30b7bdc24c66.png)

The Inter Quantile Range of Reviews is between 50 and 750 approx., then the Marketing Team should aim for Coffee Shops that have this number of Reviews.


### How does the number of reviews vary across each place type?

Plotting all histogram of Reviews by each type of Place

![reviews_Coffee_Shop](https://user-images.githubusercontent.com/56371747/198422418-c694e744-871e-4b6a-a9af-7047c3294396.png)

![reviews_Cafe](https://user-images.githubusercontent.com/56371747/198424271-dd54c3a8-6705-4e78-b65b-7c7fd4f6d2f5.png)

![reviews_Espresso_bar](https://user-images.githubusercontent.com/56371747/198424284-b7190f24-309c-4426-b76d-087ba3cb4d4a.png)

![reviews_Others](https://user-images.githubusercontent.com/56371747/198433822-def443bd-e20b-412c-acf7-f697e5a355c4.png)

As we see, Coffee Shop has a higher mean of reviews between place types,

![num_reviews_across_each_type_shop](https://user-images.githubusercontent.com/56371747/198068550-b6b072de-cdca-4085-b048-859bf7fe34e2.png)

even though the Coffee Shop Inter Quantile Range is smaller than the Cafe IQR and the IQR of Espresso bar. Maybe because the number of Coffee Shops within the dataset is almost double than the number of Cafes and almost five times the number of Espresso bars. So the recommendation is to focus, also, on those Cafe and Espresso bar places with above 500 reviews, not only Coffee Shops with between 50 and 750 reviews.


### Recomendations

If the main idea of Marketing Team is to reach more customers, then they should focus on:

- Coffe Shops around 500 reviews
- Consider also Cafes and Espresso bars, also above 500 reviews

