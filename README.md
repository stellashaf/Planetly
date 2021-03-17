# Planetly
prediction of the temperature of the cities  
Given data: average monthly temperature of different cities over the world. The longitute and latiture is alos given. 
We have to predict the temperature of cities. 
To run the code: download the jupyter note book with Python3 enviroment and use the data files "GlobalLandTemperaturesByCity.csv" and "GlobalLandTemperaturesByCountry.csv". 
The model is based on "Window Method": to make a prediction we need to know the temperature vlaues of previous 5 months window (tunable). 
Then we add the features longitude and latitute to it. 
Random forest regressor performed best. Note that we trained the model on a slice of the data, since running on full data was taking too long. 
