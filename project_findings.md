# Data Science Final Project
#### Team: Data Dealers - Julia Aguiar, Charlie Ding, Connie Wu, Luis Bueno
#### December 7th, 2019
#### Professor Grant Long

### Data Usage
(a) What outside data have you appended to the original data set? Why did you choose this data?
> We wanted to use outside data that was not necessarily connected to real estate or rental prices. 
We initially came up with a few different things that could cause a change in rent prices, such as crime, quantity of 
commercial establishments, number of parks, school districts, amongst others. 
We settled in two additional data sources:
>  - DOHMH New York City Restaurant Inspection Results (from week 3 of class)
We choose these data because we believe that the number of commercial places in a region (zip code) plays a role in the pricing of 
apartments. First, we calculated the number of restaurants located within a certain zip code. With this, we joined the restaurant 
data to the original data set on the zip column. This added one additional column to our Test3 data - Restaurant Count. 
We used this count as a parameter for our model.
>  - Walk-to-a-Park Service area ([dataset source](https://data.cityofnewyork.us/Recreation/Walk-to-a-Park-Service-area/5vb5-y6cv)).
Similarly to the restaurant count, we thought that the number of parks in a region could add value to apartments. 
We made the same calculation as with restaurants and added a Park Count to the Test3 data, which was also used as feature in our model.

(b) Does the inclusion of this additional data raise any ethical considerations? 
> The inclusion of these additional data does not raise any ethical considerations.  

### Data Exploration
(a) What outliers present issues for your analysis? How have you chosen to handle them? Why? 
> There were outliers in the feature ‘min_to_subway’. We chose to investigate each one individually as there were only five. 
We found the correct values from a google search and replaced the outliers on our data set.

(b) To what extent do missing values pose a challenge for your analysis? How have you chosen to handle them? Why? 
> ```Min_to_subway``` feature had 16 missing values. We chose to handle them by manually searching and replacing the values on the data set.

(c) Are there any other aspects of the data your exploration shows might be problematic? 
> No, there were no other aspects of the data exploration which were problematic. 

(d) Create at least one visualization that demonstrates the predictive power of your data. 
> This is a scatter plot of square footage by rent price based on the training data set. As we can see, this is a good feature for 
predictions using a linear regression model.

# Insert Image!!!

### Transformation and Modeling
(a) Describe 5 features you think to play the biggest role in your model. 
> - Bedrooms - Number of bedrooms in the property. Feature belonged to the original data set
> - Bathrooms - number of bathrooms in the property, Feature belonged to the original data set
> - Square Footage - Number of bathrooms in the property, Feature belonged to the original data set
> - Minutes to Subway - number of bathrooms in the property, Feature belonged to the original data set
> - Number of Restaurants in Zip Code - starting from the restaurant data given on week 3 of class, we counted the number of restaurants per zip code. 
Then we exported the data as a frame with two columns: zip codes and count.
We joined the Test3 data to this external data source on Zip Codes and used count as a feature.
> - Number of Parks in Zip code - using the “Walk-to-a-Park Service area” dataset ([source](https://data.cityofnewyork.us/Recreation/Walk-to-a-Park-Service-area/5vb5-y6cv)), we computed the number of parks within a zip code. 
From there we joined the Test3 and restaurant data along with this external data set on zip code and used NumParks as a feature. 

(b) Describe how you are implementing your model. Why do you think this works well? 
> We implemented the model as a random forest regressor. We believe this is a great improvement from our previous model which used a simple linear regression.

(c) Describe your methodology for selecting your model. Why do you think this type of model works well? 	
> At first, we thought about using a classification model. However, we believed that we could achieve good results using a regression model because the target, rent, is continuous. 

### Mertics, Validation, and Evaluation
(a) How well do you think your model will perform on the holdout test set? How do you know? 
> We believe it will perform better than our previous model but we are not sure how much better. 

(b) Is your model useful? Why or why not? 
> We believe our model is somewhat useful in predicting rents. Although it probably won’t be super precise, it can still give us a rough estimate of rents in New York.

(c) Are there any special cases in which your model works particularly well or particularly poorly?
> The more features we add to our model, the worse it performs. Which is why we choose to go with a small number of features.

(d) Create at least one visualization that demonstrates the predictive power of your model. 
> We plotted a histogram of rents. As expected, it is right-skewed as the majority of rentals fall under the $5k/month, while outliers can go up to $25k/month

# Insert image!!!


### Conclusion
(a) How would you use this model? 
> To predict rental prices in New York. If we choose to use it for other areas we would have to adjust the data to reflect the change. 
For example, if we used this model for Seattle, we would have to use data from Seattle restaurants and similar data from Street Easy but with Seattle apartments. 

(b) If you could have additional modeling features, what would they be?
> Maybe something to do with crime and school districts in a given region. Although we believe that crime data could affect rental prices, 
we believe that school district data might affect real estate prices more than it would affect rent. 

(c) Would you rather have more data or more features?
> More data. We only added a single feature per external data source to our model.


