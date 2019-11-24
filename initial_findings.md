# NYC Rent Predictor

### Team: Data Dealers 
#### (Julia, Connie, Luis, Charlie)

1. A 200-300 word explanation of the expected performance of the model in terms of mean squared error and the key features driving the team’s modeling performance.

>  Our model is driven by the following key feature parameters: 
  ```'bedrooms', 'bathrooms', 'min_to_subway', 'size_sqft'```.
  We picked these values because we determined that they positively impacted the model performance when we isolated them; while also using personal experience and common sense to deduce the features. Using linear regression, our mean squared error is 4191323.076233124, which is slightly below the required for this iteration of the project. 
  During this part of the analysis, we have excluded values that are not integers. However, we are considering using these during the next phase of our project in a classification model.


2. A 200-300 word summary outlining the team’s intended strategy to improve the predictions for the final round.

>  Our team’s intended strategy to improve the predictions for the final round is to try using a classification model using the 'boroughs' parameter. 
  We believe that the location of the apartment or house play a significant part in rent prices. 
  Additionally, we expect our auxiliary data frame, Housing New York Units By Building, obtained from NYC Open Data to help improve our model. 
  From this data set, we can extract the boroughs and train the data for each of the 5 boroughs. Although we have found this data set promising, we are still searching for other possible sets that could be helpful. We are also considering further exploring location as a feature by exploring a classification model that uses the neighborhoods rather than just boroughs, for a more granular approach. 
  Since we intend on trying a classification model, we will be examining the additional features from datasets that could assist in our goal. Our strategy will most likely develop and evolve as we continue to research and test different ways to improve our rent predictions for the final round. 

