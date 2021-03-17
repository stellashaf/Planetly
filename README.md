# Planetly
## Prediction of the temperature of the cities  

- Given data: average monthly temperature of different cities over the world. The longitute and latiture of cities is also given. 

-  We have to predict the temperature of cities. 
- To run the code: download the jupyter note book with Python3 enviroment and use the data files "GlobalLandTemperaturesByCity.csv" and "GlobalLandTemperaturesByCountry.csv". 
- Model 
  - The predictive model is based on "Window Method": to make a prediction we need to know the temperature vlaues of previous 5 months window (tunable). 
  - Then we add the features longitude and latitute to it. 
Random forest regressor performed best. Note that we trained the model on a slice of the data, since running on full data was taking too long. 

  - To find the top 4 cities with maximum temperature variation in a specified time period, we used a random time period of "start_date = '1990-1-1'" and "end_date = '2005-1-1'". 
  - Temperature prediciton is made on these 4 cities. 
- Preprocessing:
  - Data cleaning; We repaced the nan values of temperature with average of next and previous valid values. 
  - Extraced the numeric values of Longitiute and Latitute to use them as feature. 
  - Extracted the month and year fromt eh date column, for calculation of "decades". 

- Observations: For each city: We calculated the max values for each decade. Then we took the difference of max and min over the decades. We observed that some data points are too high. They are outliar. We removed thme to calculate the highest variability in AverageTemperature. 
