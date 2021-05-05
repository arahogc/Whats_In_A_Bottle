# Whats_In_A_Bottle


**Link to Tableau Analysis:** [What's in a Bottle](https://public.tableau.com/profile/paige.spiller#!/vizhome/WineryLocations_16198920961010/WhatsinaBottleStory)


![points_stats.PNG](Resources/points_stats.PNG)
![points_range.PNG](Resources/points_range.PNG)

![price_stats.PNG](Resources/price_stats.PNG)
![price_range.PNG](Resources/price_range.PNG)

![country_list.PNG](Resources/country_list.PNG)

### Description of how data was split into training and testing sets
#### training size = .8 (will add more)

### Explanation of model choice, including limitations and benefits
#### Decision Tree Classifier (will add more)

### how does the model address the initial question?
(will add more - will speak to correlations found/weight of features/how this relates back to question)

## Machine Learning Model Results:

## Wine Trends by Points:
![points_model.PNG](Resources/points_model.PNG)

![points_features.PNG](Resources/points_features.PNG)

## Wine Trends by Price:
![price_model.PNG](Resources/price_model.PNG)

![price_features.PNG](Resources/price_features.PNG)

## Wine Trends by Country:
![country_model.PNG](Resources/country_model.PNG)

![country_features.PNG](Resources/country_features.PNG)

## Wine Trends by Country (second model):
#### We decided to run the Country model again after dropping all location specific data - as these features had over 85% weight and resulted in a 97% accuracy, 92% average precision, and 92% average recall in the original Country model. The following shows the results after dropping location specific data:
![country2_model.PNG](Resources/country2_model.PNG)

