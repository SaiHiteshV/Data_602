# Data_602

## Problem Statement
Trip duration is the most fundamental measure in all modes of transportation. Hence, it is crucial to predict the trip-time precisely for the advancement of Intelligent 
Transport Systems (ITS) and traveller information systems. Data mining techniques are employed in this paper to predict the trip duration of rental bikes in Seoul Bike sharing system. The rental duration prediction needs to be carried out with the combination of Seoul Bike data and weather data.

## About the Data
The Data used include trip duration, trip distance, pickup-dropoff latitude and longitude, temperature, precipitation, wind speed, humidity, solar radiation, snowfall, 
ground temperature and 1-hour average dust concentration.

# https://www.kaggle.com/saurabhshahane/seoul-bike-trip-duration-prediction

Due to system limitations I could only access 1.5 million records out of 9.6 million records and performed EDA on it.

## Observations
In the given dataset there are 2 types of data. They are numerical and categorical. The columns Pmonth, Pday, Phour, Pmin, PDweek, Dmonth, Dday, Dhour, Dmin, DDweek are categorical and the columns Duration, Distance, Haversine, Temp, Precip, Wind, Humid, Solar, Snow, GroundTemp, Dust are numerical.

The duration column is in minutes and the distance column is in meters.

The Duration, Distance, Haversine are right-skewed and Temp, Wind, Humid, GroundTemp have a normal distribution.

Based on the insights from various graphs it looks like people who rent the bikes are using them to travel to offices(jobs).

## Interpretation model
- The model has an overall explanatory power of 81%.
- For the above model const, Pmonth, Pday, Phour, Dmonth, Dday,Dhour columns are significant.
- The columns PLong, PLatd, DLong, DLatd, PDweek, DDweek , Temp, Precip, Wind, Humid, Solar, Snow, GroundTemo and Dust play less significant role.
- We can observe that there are few misfits in the data. This might be because the model is highly dependent on few columns like Pmonth and Dmonth. With a small change in these column values the prediction is greately affected.
- The RMSE of the model is 10.48.

## Predictive models
- The OLS model has an overall explanatory power of 95.6%
- The RMSE of the OLS model is 5.61 minutes which is nearly half of that of the previous OLS model.
- The Linear regression model has an overall explanatory power of 94.8%
- The RMSE of the Linear regression model is 5.41 minutes.
- Most of the residuals for Linear regression model are 0.
- Ridge regression model at lambda = 0 acts as a simple linear regression.
- The Ridge regression model has an overall explanatory power of 94.8%
- The RMSE of the Ridge regression model is 5.41 minutes which is nearly equal to that of the Linear regression model.
- As the value of alpha keeps increasing for Ridge regression model most of the coefficients tend to move towards 0 i.e. come close to 0.
- The R-squared value of the Ridge regression model keeps decreasing as the alpha value increases, this might be because we might be oversimplifying the model too much.
- As the value of alpha keeps increasing for Lasso Regression all of the coefficients tend to become 0 we can observe this when alpha = 50.
- The R-squared value of the Lasso Regression model keeps dropping as we keep on increasing the $\alpha$ value and becomes 0 when alpha = 50.
